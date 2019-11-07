> json 배열 이용방법

1. json데이터 생성 및 ajax function 호출
- source
 chkTab05.each(function(idx,ele){
  jsonO.board_seq = $(ele).val();
  jsonO.sort = $(ele).next().val();
  jsonArr.push(jsonO)
 }
 ajax_sync(url, callback, JSON.stringfy({"data":jsonArr}));
 // jsonO1.data=jsonArr;  
 // ajax_sync(url,callback,JSON.stringify(jsonO1));
 // ajax_sync(url,callback,JSON.stringify({"data":json01}));
 
 
 2. ajax function - 배열일 경우 contentType:"application/json" 
 - source
 $.ajax({ url:, type:, dataType:"json", data:param, //contentType:"application/json"  --1차원 맵은 없어도 됨, 배열이 추가될 경우 필요
 
 3. Controller
 - source
 @ResponseBody
 public Object settingPart(@RequestParam Map<String, Object> params) throws   // 배열일 경우 @RequestBody 



reactive stream  - db (메모리 DB)
elasticsearch 캐싱 데이터 가져온거
