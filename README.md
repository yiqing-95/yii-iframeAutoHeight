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

