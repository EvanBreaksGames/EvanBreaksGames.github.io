/*BEGIN SN30 Pro Controller Styling*/
/*This class defines the base attributes of the skin*/
.controller.custom{
    /* The background image is basically the base for the controller's skin. The 
    PS3 controller's skin can be found at http://mrmcpowned.com/gamepad/ps3-assets/base.png
    and you can observe it as an example. The sticks, buttons, and directional arrows are missing
    because their appropriate elements will be incorperated when their styling is defined below.
    The entirity of the skin's visual styling is done via background images and CSS sprites. */ 
    background: url(https://i.imgur.com/luvntOw.png); 
    height: 555px;
    width: 1084px;
}
.custom.disconnected { /* This class shows an image when the controller is disconnected */
    background: url(https://i.imgur.com/eB7RNt7.png);
}
/* This hides the controller's button when disconnected so only the background image remains */ 
.custom.disconnected div {
    display: none;
}
.custom .triggers{ /* The triggers are housed inside a div, so this sizes the div properly and positions it */
    width: 856px;
    height: 71px;
    position: absolute;
    left: 112px;
}
.custom .trigger{/* These are the actual triggers themselves */
    width:235px;
    height:71px;
    background: url(https://i.imgur.com/r1HyxFG.png);
    opacity: 0;
}
/* The left and right classes below are used to position the triggers
within the div they're contained in. Since their positions is realtive
to the size of the parent element, we simply resize the parent element 
above to achieve the desired position. */
.custom .trigger.left{ 
    float: left;
}
.custom .trigger.right{
    -webkit-transform: rotateY(180deg);
    transform: rotateY(180deg);
    float: right;
}

/* The bumpers follow the same methodology as the triggers in terms of
placement */
.custom .bumper{
    width: 239px;
    height: 48px;
    background: url(https://i.imgur.com/4wEkGQz.png);
    opacity: 0;
}
.custom .bumpers{
    position: absolute;
    width: 863px;
    height: 48px;
    left: 110px;
    top: 80px;
}
.custom .bumper.pressed{ /* The '.pressed' class is used for most buttons to signify they've been pressed */
    opacity: 1;
}
.custom .bumper.left{
  /* Call me lazy or smart, but why should I make 2 bumpers when they're symmetrical
  and I can just rotate them in the browser? Also, note that you most likely won't need
  to use a browser speficic prefix unless it's something that is indeed browser specific.
  NOTE: CLR Browser is basically chrome, so you use '-webkit-' as the browser prefix. */
    float: left;
}
.custom .bumper.right{
    -webkit-transform: rotateY(180deg);
    transform: rotateY(180deg);
    float: right;
}
/* This bit of code is for the player indicator, which is represented in
quandrants on the xbox controller. That's note what it's called on the
PS3 controller but it'd be pointless for me to change the HTML for 
something as pedantic as a name. */
.custom .quadrant{
    position: absolute;
    background: url(ps3-assets/player-n.png);
    height: 17px;
    width: 111px;
    top: 140px;
    left: 240px;
}
/* Since the player indicator is just a CSS sprite, we change the 
position of the background to match the player number.
NOTE: Player orderin starts at 0, so p0 = Player 1 */
.custom .p0{
    background-position: 0 -6px;
}
.custom .p1{
    background-position: 0 -28px;
}
.custom .p2{
    background-position: 0 -49px;
}
.custom .p3{
    background-position: 0 -70px;
}
/* This is to size and position the containing div for the 
start and select buttons. */
.custom .arrows{
    position: absolute;
    width: 193px;
    height: 65px;
    top: 237px;
    left: 405px;
}
/* Setting the size and CSS sprite for the start adn select buttons */
.custom .back, .custom .start{
    background: url(https://i.imgur.com/hXBuheC.png);
    width: 75px;
    height: 65px;
    opacity: 0;
}
.custom .back.pressed, .custom .start.pressed{
    opacity: 1;
}
.custom .back{
    float: left;
}
.custom .start{
    float: right;
    background-position: 75px 0;
}
/* Positioning and size of the container for the face buttons */
.custom .abxy{
    position: absolute;
    width: 287px;
    height: 241px;
    top: 151px;
	right: 77px;
}
/* base class used to simplify the sprite mapping */
.custom .button{
    position: absolute;
    width: 82px;
    height: 81px;
    background: url(https://i.imgur.com/M1cZ5lq.png);
    opacity: 0;
}
.custom .button.pressed{
    opacity: 1;
}
.custom .a{
    top: 160px;
    left: 102px;
}
.custom .b{
    top: 80px;
    left: 205px;
}
.custom .x{
    top: 80px;
    left: 0;
}
.custom .y{
    top: 0;
    left: 102px;
}
/* Analog sticks follow the same principles as the triggers in terms of positioning
Note that the rotation of the sticks in hard coded with javascript, so it applies 
the CSS inline. */
.custom .sticks{
    position: absolute;
    width: 446px;
    height: 134px;
    top: 368px;
    left: 317px;
}
.custom .stick{
    position: absolute;
    background: url(https://i.imgur.com/KjLJe1V.png);
    background-position: 0 0;
    height:134px;
    width: 135px;
}
.custom .stick.pressed{
    background-position: 135px 0;
}
.custom .stick.left{
    top: 0;
    left: 0;
}
.custom .stick.right{
    top: 0;
    left: 310px;
}
/* Dpad possitioning and sizing */
.custom .dpad{
    position: absolute;
    width: 191px;
    height: 191px;
    top: 176px;
    left: 124px;
}
.custom .face{
    /*background: url(https://i.imgur.com/9yG0Ik7.png);*/
    position: absolute;
    opacity: 0;
}
.custom .face.up{
	background: url(https://i.imgur.com/W0iFlZq.png);
    left: 75px;
    top: 14px;
    /*background-position: 74px 14px;*/
	width: 42px;
	height: 39px;
}
.custom .face.down{
	background: url(https://i.imgur.com/BigVz5n.png);
    left: 75px;
    top: 138px;
    /*background-position: 74px 138px;*/
	width: 42px;
	height: 39px;
}
.custom .face.left{
    background: url(https://i.imgur.com/ide2Bdm.png);
	top: 75px;
    left: 13px;
    /*background-position: 13px 75px;*/
	width: 39px;
	height: 42px;
}
.custom .face.right{
    background: url(https://i.imgur.com/rSd5seW.png);
	top: 75px;
    left: 139px;
    /*background-position: 138px 75px;*/
	width: 39px;
	height: 42px;
}
.custom .face.pressed{
    opacity: 1;
}
/* The following entries are empty because I haven't used them yet, but they
exist for the purpose of displaying a fightstick. Since fightsticks have 
the left and right triggers and digital buttons, there are separate 
html items that allow the triggers to be shown as button presses isntead of
an opacity setting */
.custom .trigger-button.left{
    
}
.custom .trigger-button.right{
    
}
.custom .trigger-button.left.pressed{
    
}
.custom .trigger-button.right.pressed{
    
}
/* This is where the fight stick CSS would go. The ideal way of 
showing the input would be to use an image sprite of a fight stick in
all 8 positions, and change it according to the inputs. The classes 
themselves are fairly self explanatory. */
.fstick{
    position: absolute;
    width: 140px;
    height: 132px;
    top: 192px;
    left: 74px;
}
.fstick.up{
  
}
.fstick.down{
  
}
.fstick.left{
  
}
.fstick.right{
  
}
.fstick.up.right{
  
}
.fstick.up.left{
  
}
.fstick.down.right{
  
}
.fstick.down.left{
  
}
/*END SN30 Pro Controller Styling*/
