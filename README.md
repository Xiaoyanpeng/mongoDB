# mongoDB
分布式存储数据库
创建数据目录
    D:\mongo\data\db
    D:\mongo\data\log
运行服务器
定位到bin位置
mongod.exe --dbpath d:\mongo\data\db
mongod.exe --logpath "d:\mongo\data\log\mongodb.log" --logappend --install

运行CMD需要是管理员身份，右键选择
net start mongodb
mongo
//进入对MongoDB进行操作和管理的交互式环境
use first 
db.students.find().pretty()//列举数据

npm使用
npm install mongoose --save
var db=require('mongoose');
db.connect("mongodb://localhost/form");
var Dog=db.model('Dog',{
  number:{
    type:String,
    default:""
  },
  name:{
    type:String,
    default:''
  }
})
module.exports={Dog:Dog};
