> json 배열 이용방법

1. json데이터 생성 및 ajax function 호출
- source
 chkTab05.each(function(idx,ele){
  jsonO.board_seq = $(ele).val();
  jsonO.sort = $(ele).next().val();
  jsonArr.push(jsonO)
 }
 ajax_sync(url, callback, {"data":JSON.stringfy(jsonArr)});
 // jsonO1.data=jsonArr;  
 // ajax_sync(url,callback,JSON.stringify(jsonO1));
 // ajax_sync(url,callback,JSON.stringify({"data":json01}));
 
 
 2. ajax function
 - source
 $.ajax({ url:, type:, dataType:"json", data:param, //contentType:"application/json"   주석처리 됨
 
 3. Controller
 - source
 @ResponseBody
 public Object settingPart(@RequestParam Map<String, Object> params) throws
