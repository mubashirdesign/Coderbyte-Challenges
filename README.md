# Coderbyte-Challenges
My answers/logic to the Coderbyte quiz challenges.


////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
1. Find the longest word in a string:

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
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
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
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
3. Reverse the string input

        function FirstReverse(str) { 
        //"hello"
        //convert string into array
        const stringArray = str.split('').reverse().join(''); // "olleh"
        return stringArray; 
        }

FirstReverse(readline());
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
4. Replace the characters based on algorithm

        function LetterChanges(str) { 
        //replace the characters by adding 1 to the ascii code making it go from a to b, b to c, and so on
        //replace using regex to select a to z, run the callback function to run the algorithm
        //use the iteneray operator to set Z to a because adding + 1 to Z's ascii code will not make it A

        const newStr = str.replace( /[a-z]/gi,(char) => { 
        return (char === 'z' || char === 'Z') ? 'a' : String.fromCharCode(char.charCodeAt() + 1); 
         });

        //replace using regex to select all vowels
        //use the call back function to uppercase the selected regex expression

        const strFinal = newStr.replace(/a|e|i|o|u/gi, (vowel) => { 
        return vowel.toUpperCase();
        });

        // return the final string

        return strFinal; 
        }

LetterChanges(readline());
