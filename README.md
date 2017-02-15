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

function DOMEval(code,doc){
    doc=doc||document;
    var script=doc.createElement("script");
    script.text=code;
    doc.head.appendChild(script).parentNode.removeChild(script);
}
var version="3.1.1", 
     jQuery=function(selector,context){
        return new jQuery.fn.init(selector,context);
     },
     rtrim=/^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g
     rmsPrefix=/^ms-/,
     rdashAlpha=/-([a-z])/g,
     fcamelCase=function(all,letter){
       return letter.toUpperCase();
     }
     
     jQuery.fn=jQuery.prototype={
          jquery:version,
          constructor:jQuery,
          length:0,
          toArray:function(){
             return slice.call(this);
          }
     }
     
     get:function(num){
        if(num == null){
            return slice.call(this);
        }
        return num<0?this[num+this.length]:this[num];
     },
     pushStack:function(elems){
        var ret = jQuery.merge(this.constructor(),elems);
        ret.pervObject = this;
        return ret;
     },
     each:function( callback ) {
         return jQuery.each( this, callback );
     },
     map: function( callback ) {
        return this.pushStack( jQuery.map( this, function( elem,i ) {
           return callback.call( elem, i, elem);
        }))
     },
     
     slice:function() {
          return this.pushStack( slice.apply( this, arguments ) );
     },
     first: function() {
        return this.eq(0);
     },
     last:function() {
        return this.eq(-1);
     },
     eq: function() {
          var len=this.length,
              j=+i+(i<0?len:0);
              return this pushStack( j >= 0 && j<len ? [ this[ j ] ]: [] ) ;
    },
    
    end: function() {
       return this.provOject || this.constructor() ;
    }
