# friends

&lt;div class=&#34;linkpage&#34;&gt;&lt;ul id=&#34;friendsList&#34;&gt;&lt;/ul&gt;&lt;/div&gt;

&lt;!-- ## 交换友链

如果你觉得我的博客有些意思，而且也有自己的独立博客，欢迎与我交换友链~

可通过 [Issues](https://github.com/ryan4yin/ryan4yin.space/issues) 或者评论区提交友链申请，格式如下：

    站点名称：Ryan4Yin&#39;s Space
    站点地址：https://ryan4yin.space/
    个人形象：https://www.gravatar.com/avatar/2362ce7bdf2845a92240cc2f6609e001?s=240
    站点描述：赞美快乐~ --&gt;


&lt;script type=&#34;text/javascript&#34;&gt;
// 以下为样例内容，按照格式可以随意修改
var myFriends = [
    [&#34;https://leviathanwz.github.io/&#34;, &#34;https://leviathanwz.github.io/images/avatar.png&#34;, &#34;leviathanwz&#34;, &#34;&#34;], 
    [&#34;https://yuirito.github.io/&#34;, &#34;https://yuirito.github.io/images/avatar.jpg&#34;, &#34;yuirito&#34;,&#34;&#34;], 
    [&#34;https://ooopig.github.io/&#34;, &#34;https://ooopig.github.io/img/favicon1.png&#34;, &#34;ooopig&#34;, &#34;&#34;], 
];



// 以下为核心功能内容，修改前请确保理解您的行为内容与可能造成的结果
var  targetList = document.getElementById(&#34;friendsList&#34;);
while (myFriends.length &gt; 0) {
    var rndNum = Math.floor(Math.random()*myFriends.length);
    var friendNode = document.createElement(&#34;li&#34;);
    var friend_link = document.createElement(&#34;a&#34;), 
        friend_img = document.createElement(&#34;img&#34;), 
        friend_name = document.createElement(&#34;h4&#34;), 
        friend_about = document.createElement(&#34;p&#34;)
    ;
    friend_link.target = &#34;_blank&#34;;
    friend_link.href = myFriends[rndNum][0];
    friend_img.src=myFriends[rndNum][1];
    friend_name.innerText = myFriends[rndNum][2];
    friend_about.innerText = myFriends[rndNum][3];
    friend_link.appendChild(friend_img);
    friend_link.appendChild(friend_name);
    friend_link.appendChild(friend_about);
    friendNode.appendChild(friend_link);
    targetList.appendChild(friendNode);
    myFriends.splice(rndNum, 1);
}
&lt;/script&gt;


&lt;style&gt;

.linkpage ul {
    color: rgba(255,255,255,.15)
}

.linkpage ul:after {
    content: &#34; &#34;;
    clear: both;
    display: block
}

.linkpage li {
    float: left;
    width: 48%;
    position: relative;
    -webkit-transition: .3s ease-out;
    transition: .3s ease-out;
    border-radius: 5px;
    line-height: 1.3;
    height: 90px;
    display: block
}

.linkpage h3 {
    margin: 15px -25px;
    padding: 0 25px;
    border-left: 5px solid #51aded;
    background-color: #f7f7f7;
    font-size: 25px;
    line-height: 40px
}

.linkpage li:hover {
    background: rgba(230,244,250,.5);
    cursor: pointer
}

.linkpage li a {
    padding: 0 10px 0 90px
}

.linkpage li a img {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    position: absolute;
    top: 15px;
    left: 15px;
    cursor: pointer;
    margin: auto;
    border: none
}

.linkpage li a h4 {
    color: #333;
    font-size: 18px;
    margin: 0 0 7px;
    padding-left: 90px
}

.linkpage li a h4:hover {
    color: #51aded
}

.linkpage li a h4, .linkpage li a p {
    cursor: pointer;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
    line-height: 1.4;
    margin: 0 !important;
}

.linkpage li a p {
    font-size: 12px;
    color: #999;
    padding-left: 90px
}

@media(max-width: 460px) {
    .linkpage li {
        width:97%
    }

    .linkpage ul {
        padding-left: 5px
    }
}

&lt;/style&gt;

