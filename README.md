The simplest way to hide the keyboard in xCode is to have your UIView subclass UIControl.<br />
<br />
An simple example: <br />
<div class="separator" style="clear: both; text-align: center;">
<a href="http://4.bp.blogspot.com/-a3HgDOoQRDU/VLRPQWHAeQI/AAAAAAAACrk/L_G-3ftoPk0/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B5.36.02%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://4.bp.blogspot.com/-a3HgDOoQRDU/VLRPQWHAeQI/AAAAAAAACrk/L_G-3ftoPk0/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B5.36.02%2BPM.png" height="400" width="640" /></a></div>
<br />
<br />
<b>Embedding a UIView in a ScrollView</b><br />
Start with a fresh View Controller. Make a new ViewController.swift class and <br />
<br />
1. Drag a ScrollView onto the UIView, make sure it cover the entire UIView.<br />
<br />
2. Drag another UIView onto the ScrollView, covering the entire view. Add your UI objects to this UIView. The Document Outling should look like this:<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="http://3.bp.blogspot.com/--A277ANDHa8/VLRmrk6cGuI/AAAAAAAACso/S8NRyZOce54/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B7.28.07%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://3.bp.blogspot.com/--A277ANDHa8/VLRmrk6cGuI/AAAAAAAACso/S8NRyZOce54/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B7.28.07%2BPM.png" height="195" width="200" /></a></div>
<div class="separator" style="clear: both; text-align: center;">
</div>
<div class="separator" style="clear: both; text-align: center;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
Follow the step on the image.</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://3.bp.blogspot.com/-8RHTQXYRfvk/VLRpQ0AqWqI/AAAAAAAACtI/sdx-1VEwJWc/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B7.34.42%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://3.bp.blogspot.com/-8RHTQXYRfvk/VLRpQ0AqWqI/AAAAAAAACtI/sdx-1VEwJWc/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B7.34.42%2BPM.png" height="400" width="640" /></a></div>
<div class="separator" style="clear: both; text-align: center;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
&nbsp;<b>Auto Layout Fun.</b> </div>
<div class="separator" style="clear: both; text-align: left;">
5. In the Document Outline select the Scroll View<b> </b>=&gt; Editor =&gt; Align =&gt; Horizontal Center In Container as shown below.&nbsp;</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://1.bp.blogspot.com/-xZt3wiYKc50/VLR5J1NYCwI/AAAAAAAACwA/Pw6aDzx4k5M/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B8.44.07%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/-xZt3wiYKc50/VLR5J1NYCwI/AAAAAAAACwA/Pw6aDzx4k5M/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B8.44.07%2BPM.png" height="400" width="640" /></a></div>
<div class="separator" style="clear: both; text-align: left;">
6. Select the UIControl View and do the same.</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
7. Select both text fields and do the same.</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
8. Starting from the top, use the pin tool to pin each text field's top, left and right spacing as well as the height as shown below. On the bottom text field also pin the bottom spacing, it will not work unless you do this. See below.</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://2.bp.blogspot.com/-0nxkwHupJlk/VLR7ZuU3SpI/AAAAAAAACwQ/w8vBDtR00cs/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B8.52.57%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://2.bp.blogspot.com/-0nxkwHupJlk/VLR7ZuU3SpI/AAAAAAAACwQ/w8vBDtR00cs/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B8.52.57%2BPM.png" height="400" width="640" /></a></div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<b>ViewController class setup</b><br />
<div class="separator" style="clear: both; text-align: left;">
6. Set the class of the view controller as shown below.</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://1.bp.blogspot.com/-PHq-Wi_vfSw/VLR-wFiGQOI/AAAAAAAACwc/jv69InnPgK0/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B9.01.02%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://1.bp.blogspot.com/-PHq-Wi_vfSw/VLR-wFiGQOI/AAAAAAAACwc/jv69InnPgK0/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B9.01.02%2BPM.png" height="400" width="640" />&nbsp;</a></div>
<div class="separator" style="clear: both; text-align: left;">
&nbsp;7. Bring up the assistant editor, it should show the ViewController.swift file. Control drag from each text field object to the where you see the @IBOutlets in the screenshot below.  Create the Connections. Manually copy the @IBAction method I have provided. </div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://2.bp.blogspot.com/-BiTghb5bAAU/VLSAJRYvFxI/AAAAAAAACwo/WV5jyBOtj_4/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B9.16.59%2BPM.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://2.bp.blogspot.com/-BiTghb5bAAU/VLSAJRYvFxI/AAAAAAAACwo/WV5jyBOtj_4/s1600/Screen%2BShot%2B2015-01-12%2Bat%2B9.16.59%2BPM.png" height="400" width="640" /></a></div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
&nbsp;8. Control drag from the UIControl View in the Document Outline to the View Controller object in the Document Outline, select background touch.&nbsp;</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
9. That's it. It should be ready to run.</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
GitHub Project link&nbsp;</div>
<div class="separator" style="clear: both; text-align: left;">
https://github.com/jsavage06/iOSScrollviewBackgroundTouch </div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<br />
<br />
<br />
<br />
