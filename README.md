find-needles
=============


// haystack is the string and needles is the string array that each contain words
// if the number of needles in the array is greater than 5, print an error of too many words and exit

public static void findNeedles(String haystack, String[] needles){ if(needles.length > 5){
System.err.println("Too many words!");
}

// if the needle size is less than 5, it compares the haystack string over a number of characters including single quotes
// tabs, new lines, word boundries, form feeds and carriage returns into an array called words
// each needle element of array is compared to each element of the word array and if a "needle" element matches a "word" element
// a counter for the respective array is incremented.

else{
int[] countArray = new int[needles.length]; for(int i = 0; i < needles.length; i++){
String[] words = haystack.split("[ \"\'\t\n\b\f\r]", 0); for(int j = 0; j < words.length; j++){
if(words[j].compareTo(needles[i]) == 0){ countArray[i]++;
}
}
}
// after each search and compare function, each needle is displayed along with the number of times it occured in the haystack
// and once it reaches the end of all array elements the function exits.

for (int j = 0; j < needles.length; j++) { System.out.println(needles[j] + ": " + countArray[j]);
}
}
}



\\ explanation of haystack.split
\\   \"      look for double quotes
\\   \'      look for single quotes
\\   \t      look for tabs
\\   \n      look for new lines
\\   \b      word boundary (space, punctuation, etc)
\\   \f      look for form feeds
\\   \r      look for carriage returns








# google-oogle




