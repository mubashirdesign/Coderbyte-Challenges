# Coderbyte-Challenges
My answers/logic to the Coderbyte quiz challenges.


////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
1.Find the longest word in a string:

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

LongestWord(readline());
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
2. Find the First Factoral

function FirstFactorial(num) { 

const arrNumb = [];

  //Loop through the numbers to make an array of the factorials
  
 if (num > 0){    
 
     for (let i = 0; i <= num; i++ ){   
     
        arrNumb.push(i);
        
        }
        
         //shift 0 out of the array
        arrNumb.shift();
}

  //multiply each array element with the last one using reduce
  
  const factorialNumb = arrNumb.reduce((a, b) => a*b);
  
  return factorialNumb;      
  
}

FirstFactorial(readline());

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
