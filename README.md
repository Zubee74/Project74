# Project74

//promiss example
function promFunc(completed)
{
  return new Promise(function (rejected, resolved)
  {
    console.log("Fetching data, please wait...");
    setTimeout(()=>{
      if (completed)
      {
        resolved("promiss success");
      }else
      {
        rejected("promiss not success");
      }
    },2000)
  });
}
promFunc(true).then((result) => {
  console.log(result);
}).catch((error)=>{
  console.log(error);
});
  
