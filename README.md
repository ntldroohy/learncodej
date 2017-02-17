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
          },
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
    },
    push:push,
    sort:arr.sort,
    splice:arr.splice

  }
  
jQuery.extend=jQuery.fn.extend=function() {
  var options, name, src, copy, copyIsArray, clone,
      target = arguments[ 0 ] || {},
      i = 1,
      length = arguments.length,
      deep = false;
      
      if ( typeof target === "boolean" ) {
         deep = target;
         target = arguments[ i ] || {} ;
         i++
      }
      if ( typeof target !== "object" && !jQuery.isFunction( target )) {
          target =  {};  
       }
       if ( i=== length ) {
          target = this;
          i--;
       }
       for ( ;i < length; i++ ) {
          if ( ( options = arguments[ i ] ) != null ) {
             for ( name in options ) {
                src = target[ name ];
                copy = options[ name ];
                 if ( target === copy) {
                     continue;
                 }
                 
                 if ( deep && copy && ( jQuery.isPlainObject( copy) || ( copyIsArray = jQuery.isArray( copy )))) {
                     if ( copyIsArray ){
                        copyIsArray = false;
                        clone = src && jQuery.isPlainObject( src ) ? src : [] ;
                     } else {
                       clone = src && jQuery.isArray( src ) ? src : [];
                      }
                      target[ name ] = jQuery.extend( deep, clone,copy );
                 } else if ( copy != undefined ) {
                    target[ name ] = copy;
                 }
             }
          }
       }
       
       return target;
};

jQuery.extend( {
    expando: "jQuery" + ( version + Math.random() ).replace( /\D/g, ""),
    isReady:true,
    error: function( msg ) {
       throw new Error( msg );
    },
    noop: function() {},
    isFunction: function( obj ) {
        return jQuery.type( obj )  === "function";
    },
    isArray: Array.isArray,
    isWindow: function( obj ){
       return obj !=null && obj === obj.window;
    },
    isNumeric: function( obj ){
        var type = jQuery.type( obj );
        return ( type === "number" || type === "String" ) && !isNan( obj - parseFloat( obj ) );
    },
    isPlainObject: function( obj ) {
       var proto, Ctor;
       if ( !obj || toString.call( obj ) !== "[object Object]") {
           return false;
       }
       proto = getProto( obj );
       
       if ( !proto ) {
           return true;
       }
       ctor = hasOwn.call( proto, "constructor" ) && proto.constructor;
       return typeof Ctor === "function" && fnToString.call( Ctor ) === ObjectFunctonString;
    },
    
    isEmtyObject: function( obj ) {
        var name;
        
        for( name in obj) {
            return false;
        }
        return true;
    },
})
   
