# Netgram_backEnd


Instagram-clone it includes rest API of Instgram features like login , signup, create post ,delete post like,comment and follow,unfollows operations..
it uses cloudinary for storing images and storing and uses mongodb as DATABASE Storage

        DATABASE SCHEMA
        
        1) User:
  name:{
type:String,
required:true
},
email:{
type:String,
required:true
},
password:{
type:String,
required:true
},
resetToken:String,
expireToken:Date,
pic:{
type:String,
default:"https://res.cloudinary.com/cnq/image/upload/v1586197723/noimage_d4ipmd.png"
},
followers:[{type:ObjectId,ref:"User"}],
following:[{type:ObjectId,ref:"User"}]

2) post:
  title:{
type:String,
required:true
},
body:{
type:String,
required:true
},
photo:{
type:String,
required:true
},
likes:[{type:ObjectId,ref:"User"}],
comments:[{
text:String,
postedBy:{type:ObjectId,ref:"User"}
}],
postedBy:{
type:ObjectId,
ref:"User"
}
	
