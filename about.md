---
layout: page
title: About Suhui
---
# SuHui

<div id="autotype">

hello,<br />
this is suhui .<br />
</div>
<script>
$.fn.autotype = function() {
            var $tt = $(this);
            var str = $tt.html();
            var index = 0;
            $(this).html('');
            var timer = setInterval(function() {

                var current = str.substr(index, 1);
                if (current == '<')
                    index = str.indexOf('>', index) + 1;
                else
                    index++;


                $tt.html(str.substring(0, index) + (index & 1 ? '_' : ''));

                if (index > str.length){
                    clearInterval(timer);
                }
            }, 55);
    };
$("#autotype").autotype();
</script>