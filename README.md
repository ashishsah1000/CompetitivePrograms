# CompetitivePrograms
Basic data of competitive programing



```

function BinarySearch(x,e){
  var start=0,end=x.length-1;
  var mid = 0,pos=-1,pos2=0;
  while(start<=end){
    mid = parseInt((start+end)/2);

    if(x[mid]==e){
      
      pos = mid;
      console.log("mid="+mid);
      var frontNext=pos;
      var backNext=pos;
      pos2=pos;
      var arr=x;
      while(frontNext>=0){
        frontNext = BinarySearch(x=x.slice(0,frontNext),e)
//         console.log("x="+x)
        if(frontNext!=-1){
          pos=frontNext;
        }
//         console.log("fromNext="+frontNext)
      }
      console.log("arr=",arr.slice(backNext+1,arr.length))
      
      while(backNext>=0){
        backNext = BinarySearch(arr=arr.slice(backNext+1,arr.length),e)
        console.log(arr)
        if(backNext!=-1){
          pos2++;
        }
        console.log("backNext="+pos2)
      }
      break;
    }
    if(x[mid]>e){
      end=mid-1;
    }
    if(x[mid]<e){
      start= mid+1;
    }
  }
  if(pos==-1)
     console.log("not present");
  else
      console.log("present")
  return (pos+ " "+ pos2)
}

// function getTheEnds(a){
//   var st=0,end=0;
//   while()
// }


















```
