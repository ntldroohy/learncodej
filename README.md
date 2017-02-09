# learncodej
(function(global,factory){
   "use strict;
    if(typeof module==="object"&&typeof module.exports==="object"){
         module.exports=global.document?
                factory(global,true):
                function(w){
                    if(!w.document){
                        throw new Error("jQuery requires a window with a document");
                    }
                    return factory(w);
                };
    }else{
       factory(global);
    }

"})(typeof window!=="undefined"?window:this,function(window,noGlobal){
    "use strict";
    var arr=[];
    var document=window.document;
    var getProto=Object.getPrototypeOf;
    var slice=arr.slice;
    var concat=arr.concat;
    var push=arr.push;
    var indexOf=arr.indexOf;
    var class2type={};
    var toString =class2type.toString;
    var hasOwn=class2type.hasOwnProperty;
    var fnToString =hasOwn.toString;
    var ObjectFunctionString=fnToString.call(Object);
    var Suport={};
})
