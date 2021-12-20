# AntManabaApi-Document
## 本家
https://github.com/t4t5u0/ManabaCrawlerCloudFunctions
## BaseURL  
https://fun-manaba-api.azurewebsites.net/
## 機能一覧
Jsonをpostされることを前提に設計しています。  
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
## 免責事項
このApiを使って被った全ての損害、不利益に対し、私は一切の責任を負いません。  
もちろんパスワードを抜くようなコードは書いていませんが、なんらかのトラブルがあっても責任は一切負いません。  
今の所、お叱りは受けてませんが、事務局に怒られようがどうなろうが、自分で責任を持つ（共犯になる）覚悟がある人だけ使ってください。
ぞ
