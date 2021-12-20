# AntManabaApi-Document
## BaseURL  
https://fun-manaba-api.azurewebsites.net/
## 機能一覧
json={"userid":"hoge","password":"fuga"}
- /  
  課題を全て取得します。  
  オプションで{"except_id":[course_ids],"except_type":[except_types],"least":"%Y-%m-%d %H:%M"}をつかうと  
  任意のcourse_idやtask_typeで持ってくる課題を除外できます。また、leastでは、その日時より前に期日が設定されている課題を除外します。  
  正直使いどころがあまりないので、保守してませんバグだらけだと思います。
  返り値:{{"status":"success"or"failed"},{"tasks":[task]}
- /login  
  返り値:{"status":"success"or"failed"}
- /timetable  
  返り値:{{"status":"success"or"failed"},{"timetable":{"Week of day":[Course]}}
## 注意
Azureのセキュリティの関係上、Curlを使った操作はできません。
