$(document).ready(function(){
        $('.owl-carousel').owlCarousel({
          loop: true,
          margin: 10,
          nav: false,
          dots: false,
          items: 1,
          onChanged: function(event) {
            $('.owl-dot').removeClass('active');
            $('.owl-dot').eq(event.item.index).addClass('active');
          }
        });
        $('.owl-dot').click(function() {
          $('.owl-carousel').trigger('to.owl.carousel', $(this).index());
        });
        $('.owl-dot').eq(0).addClass('active');
      });
