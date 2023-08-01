# JSclick-ScrollBaseOnWidth
JavaScript anchor HTML or click event, click and scroll from the top base on width or breakpoint media query 

```JS
jQuery( () => {
	
  /*
  //Enable this comment to get winOffset!
 
  let lastScrollTop = 0;
     
	jQuery(window).on('scroll', function() {
		
        st = jQuery(this).scrollTop();
       console.log( st ); 
		
    });  */ 

   const classExtension = function( elemTarget , winOffset ) {
		
      jQuery( elemTarget ).click(function( e ) {  e.preventDefault(); jQuery( window ).scrollTop(  winOffset );  });
	
   }
	
   let winL = jQuery( window ).width();	// window.innerWidth

   // iPhone 375 
   if( winL == 375  ) {
	
     classExtension(' #element1 a ',  2170 );
     classExtension(' #element2 a ',  2730 );
     classExtension(' #element3 a ',  3455 );
	  
   }

   // iPhone 428 
   if( winL == 428 ) {
	
     classExtension(' #element1 a ',  2010 );
     classExtension(' #element2 a ',  2580 );
     classExtension(' #element3 a ',  3216 );
	  
  }
	
});

```
Also smooth scroll link here:

https://github.com/nielsoffice/JSSmoothScroll 


