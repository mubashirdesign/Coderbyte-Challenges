# Coderbyte-Challenges
My answers/logic to the Coderbyte quiz challenges.


//////////////////////////////////////////////////////////////////////////////////////////////////////
Find the longest words in a string:

function LongestWord(sen) { 

    //SPLIT STRING INTO ARRAY
    var splitWords;  
    splitWords = sen.split(/[ ,!&@#$%^&*()]+/);
    
    //Sort splitWords largest to smallest
    splitWords.sort((a,b) => {
    
     return b.length - a.length;
        
    });
    
    return splitWords[0];
}
   
   
// keep this function call here 
LongestWord(readline());
//////////////////////////////////////////////////////////////////////////////////////////////////////
