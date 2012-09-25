yii-iframeAutoHeight
====================

wrapper the jquery plugin(iframeAutoHeight) for yii


usage example :
====================
 <?php
        $this->widget('ext.iframeAutoHeight.IFrameAutoHeight', array(
                //'debug' => false ,
                'selector'=>'iframe' ,// the css selector which select the target iframe  you want apply this plugin to
                'callback'=>'js: function(callbackObject) {
                                           var m = "new size is " + callbackObject.newFrameHeight;
                                           window.console && console.log(m) || alert(m);
                                           // you can use "this" to refer the target iframe obj
                                       }'
            )
        );
        ?>
        <iframe src="http://localhost/my/yiiSpace/" name="contentFrame" id="contentFrame" width="100%" height="800px"/>

read me
=======================================
this is a wrapper for the jquery-iframe-auto-height([jquery-iframe-auto-height on github](https://github.com/house9/jquery-iframe-auto-height "jquery-iframe-auto-height")) plugin

which can set the height of an iframe to its contents height .

**note:**
now it can't handle the cross domain url .

##Requirements

test it on yii 1.1.10  , should work with other versions ..

##Usage

extract  it to protected/extensions dir .  (actually any dir if you want ) and then in your view file which contain the iframe you want to manipulate

~~~
[php]
<?php
        $this->widget('ext.iframeAutoHeight.IFrameAutoHeight', array(
                //'debug' => false ,
                'selector'=>'iframe' ,// the css selector which select the target iframe  you want apply this plugin to
                'callback'=>'js: function(callbackObject) {
                                           var m = "new size is " + callbackObject.newFrameHeight;
                                           window.console && console.log(m) || alert(m);
                                           // you can use "this" to refer the target iframe obj
                                       }'
            )
        );
        ?>
        <iframe src="http://localhost/my/yiiSpace/" name="contentFrame" id="contentFrame" width="100%" height="800px"/>


~~~


##Resources


...external resources for this extension...

 * [jquery-iframe-auto-height on github](https://github.com/house9/jquery-iframe-auto-height)
 * [yii-iframeAutoHeight](https://github.com/yiqing-95/yii-iframeAutoHeight)
 * [original plugin](http://sonspring.com/journal/jquery-iframe-sizing)