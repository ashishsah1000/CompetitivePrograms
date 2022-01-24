Read it on Medium : [Merging two sorted arrays](https://medium.com/@ashishsah1000/merge-two-sorted-arrays-f00a69a84bc5)


```
 function mergeArrays(a,b){
   
  // Remeber a,b takes sorted arrays
 var aStart=0; //pointer to a array
 var bStart=0; //pointer to b array
 var final=[];

  while(aStart<a.length && bStart<b.length){
   // loop will break if any array is checked till end
   if(a[aStart]<b[bStart]){
       final.push(a[aStart]); // push if smaller
       aStart++; //keep increasing the pointer
    }
   else{
        final.push(b[bStart]);
        bStart++;
    }
  }
 
 
 
 // simply check the array that was not used fully
 // add it to the end of the final array

  if(aStart<a.length){
    final =final.concat(a.slice(aStart));
  }
  else{
    final = final.concat(b.slice(bStart))
  }
 return(final)
}

```

So this code should do fine.
It is self-explanatory but still has a few points to mention. This Algorithm takes O(n) time to merge two sorted arrays and that's a good thing, 
far better than any n-square algorithm.
How does it work?
The point is the array is already sorted so whenever we do any comparison and push it into the final array we are sure that no other element
in any of the arrays will be smaller than the element that we pushed, so we are sure for that element position. (Read this 3 times)
Then we simply increase the pointing variable of the array whose element we pushed. To recap just push the smaller element and increase its pointer.
As soon as one of the arrays gets exhausted that means in our other array we have elements that are greater than our final array that too in sorted
order so simply concat those two arrays.
That’s it! Now we need to understand merge sort but next, we will start by understanding a few basics of Recursion.
