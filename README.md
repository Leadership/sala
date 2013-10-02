*/ Esse script foi editado por João Marcos!

para instalar adicione esse codigo aos favoritos, e após abrir a sala clique abra esse favorito:

javascript: (function () { var jsCode = document.createElement('script');jsCode.setAttribute('id', 'plugbot-js');jsCode.setAttribute('src', 'https://raw.github.com/Leadership/sala/master/README.md');document.body.appendChild(jsCode); }())

*/


if (TFLEnhanced !== undefined)
    TFLEnhanced.close();
String.prototype.equalsIgnoreCase = function(other) {
    return this.toLowerCase() === other.toLowerCase();    
};
var plugCubed,
plugBot,
TFLEnhancedModel = require('app/base/Class').extend({
    version: {
        major: 1,
        minor: 0,
        patch: 2
    },
    toString: function() { return TFLEnhanced.version.major + '.' + TFLEnhanced.version.minor + '.' + TFLEnhanced.version.patch},
    init: function(){
        this.Socket();
        var popout = require('app/views/room/popout/PopoutView');
        var Lang = require('lang/Lang');
        setTimeout($.proxy(this.initCSS,this), 1500)
        $('#button-chat-popout').click((function(){$.proxy(this.initPopout,this);}))
                var words = {
            // Syntax: 'pesquisa por palavra' : 'Replace word',
            "pontos" : "Pontos",
            "Now Playing" : "Tocando Agora",
            "tempo Restante" : "Tempo Restante",
            "Volume" : "Volume",
            "DJ atual" : "DJ Atual",
            "Aprovação multidão" : "Opnião da Galera",
            "Fan":"Fãs"
        };
        String.prototype.prepareRegex = function() {
            return this.replace(/([\[\]\^\&\$\.\(\)\?\/\\\+\{\}\|])/g, "\\$1");
        };
        Lang.ui.buttonVotePositive = "http://i.imgur.com/BOTHpTY.png";
        Lang.ui.buttonVotePositiveSelected = "http://i.imgur.com/20LiiC9.png";
        Lang.ui.buttonVotePositiveDisabled = "http://i.imgur.com/5EDGEt8.png";
         Lang.ui.buttonVoteNegative = "http://i.imgur.com/PwdUqHd.png";
        Lang.ui.buttonVoteNegativeSelected = "http://i.imgur.com/3zho0JM.png";
        Lang.ui.buttonVoteNegativeDisabled = "http://i.imgur.com/dlwZPez.png";
        Lang.ui.buttonAddThis = "http://i.imgur.com/qcWDET3.png";
        Lang.ui.buttonAddThisDisabled = "http://i.imgur.com/qcWDET3.png";  
        Lang.ui.buttonSkipThis  = "http://i.imgur.com/86IfexG.png";
        Lang.rollover.fans = "Fã"
        Lang.rollover.points = "pontos"
        Lang.messages.fanEnter = "Seu fã% NAME% acabou de entrar na sala!"
        Lang.messages.fanOf = " Agora você é fã de %NAME%"
        Lang.messages.unFanOf = "Você não é mais fã de %NAME%"
        Lang.messages.follow = "%NAME% agora é seu fã!"
        Lang.messages.welcome = "Bem-vindo ao beta plug.dj. Version %VERSION%"
        Lang.messages.cap = "Nivelamento avatares em %COUNT%"
        Lang.rollover.fans = "Fã"
        Lang.alerts.updateMesage ="plug.dj foi atualizado e requer uma atualização. Clique em OK para atualizar a página."
        Lang.ui.buttonDJPlay = "http://i.imgur.com/kwPf8pM.png";
        Lang.ui.buttonDJLeave = "http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png";
        Lang.ui.buttonDJWaitlistJoin = "http://plug.dj/_/static/images/pt/ButtonDJWaitListJoin.7d23a08.png";
        Lang.ui.buttonDJWaitlistLeave = "http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png";
        Lang.ui.buttonDJQuitShort = "http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png";
        Lang.ui.buttonDJQuit = "http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png";
        Lang.ui.buttonDJPlayShort = "http://plug.dj/_/static/images/pt/ButtonDJWaitListJoin.7d23a08.png";
 
        Lang.rollover.host = "Bosas"
        Lang.chat.help = "<strong>Chat Commands:</strong><br/>/em &nbsp; <em>Emote</em><br/>/me &nbsp; <em>Emote</em><br/>/clear &nbsp; <em>Clear Chat History</em><br/>/cap # &nbsp; <em>Limits the number of avatars rendered (1-200)</em><br/>/ts # &nbsp; <em>Chat timestamps (12, 24, 0)</em><br />/emoji on (or off) <em>Enable/disable Emojis</em><br /> /strobe on/off &nbsp; <em>Strobe light on/off</em><br /> /rave on/off &nbsp; <em>Lights out on/off</em><br />/close &nbsp; <em>Remove TFL Enhanced script</em> <br /> /Avatar number &nbsp; <em> change Halloween Avatars ( number = 1 to 13)</em> <br /> /Auto On &nbsp; <em> plugbot load </em>"
        $('#button-chat-popout').click(function(){setTimeout(function(){TFLEnhanced.initPopout()},500)})
        function isOkTag(tag) {
            return (",pre,blockquote,code,input,button,textarea".indexOf(","+tag) == -1);
        };
        var regexs=new Array(),
        replacements=new Array();
        for(var word in words) {
            if(word != "") {
                regexs.push(new RegExp("\\b"+word.prepareRegex().replace(/\*/g,'[^ ]*')+"\\b", 'gi'));
                replacements.push(words[word]);
            }
        }
        var texts = document.evaluate(".//text()[normalize-space(.)!='']",document.body,null,6,null), text="";
        for(var i=0,l=texts.snapshotLength; (this_text=texts.snapshotItem(i)); i++) {
        if(isOkTag(this_text.parentNode.tagName.toLowerCase()) && (text=this_text.textContent)) {
            for(var x=0,l=regexs.length; x<l; x++) {
                text = text.replace(regexs[x], replacements[x]);
                this_text.textContent = text;
                }
            }
        }
                this.proxy = {
            onChat: $.proxy(this.onChat, this)
        };
        API.on(API.CHAT,this.proxy.onChat)
        API.on(API.CHAT_COMMAND,this.customChatCommand)
         var a = $('#chat-messages'),b = a.scrollTop() > a[0].scrollHeight - a.height() - 20;
        a.append('<div class="chat-update"><span class="chat-text" style="color:#FF0000"><i>Novo background [By !CrεtɪnᎧ] ' + this.version.major + '.' + this.version.minor + '.' + this.version.patch + '</i></span></div>');
        a.append('<div class="chat-update"><span style="color:#FFFF00">Enter </span>  <a href="https://www.facebook.com/JoawMarKuZ/">Aqui!</a></div>')
        this.removeElements();
        if (plugCubed == undefined) $.getScript("http://plugCubed.com/compiled/plugCubed.js")
    },
    close: function(){
        var Lang = require('lang/Lang');
        $('#TFL-css').remove();
        $('#room-wheel').css('background','url("http://plug.dj/_/static/images/room_wheel2.0ea1fb92.png")');
        $('#button-vote-negative').show();
        $('#button-dj-waitlist-join').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonDJWaitListJoin.fbffc481.png); display: block;');
        $('#button-dj-waitlist-leave').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.5d5847b1.png); display: block;');
        $('#button-dj-play').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonDJPlay.742fd499.png); display: block;');
        $('#button-dj-leave').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonDJQuit.1a691d0c.png); display: block;');
        $('#dj-console').attr('style','background-image:url(http://plug.dj/_/static/images/DJConsole2.8acc86f0.png); display:block;');
        $('#button-add-this').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonAddThis.175d7d45.png);');
        $('#meta-frame').show('.frame-background');
        $('#playback').show('.frame-background');
        $('#meta-frame').css('background-color','#0A0A0A');
        $('#playback').css('background-color','#0A0A0A');
        $('body').attr('style','background-image: url(http://plug.dj/_/static/images/room_background1.91844df.jpg); no-repeat scroll center top #000000;');
        Lang.alerts.notEnoughPoints = "You don't have enough points to use that avatar.";
        Lang.ui.buttonVotePositive = "http://plug.dj/_/static/images/en/ButtonVotePositive.85cfc5a9.png";
        Lang.ui.buttonVotePositiveSelected = "http://plug.dj/_/static/images/en/ButtonVotePositiveSelected.c9947cb3.png";
        Lang.ui.buttonVotePositiveDisabled = "http://plug.dj/_/static/images/en/ButtonVotePositiveDisabled.ce7c40b3.png";
        Lang.ui.buttonVoteNegative = "http://plug.dj/_/static/images/en/ButtonVoteNegative.ef04d51.png";
        Lang.ui.buttonVoteNegativeSelected = "http://plug.dj/_/static/images/en/ButtonVoteNegativeSelected.675a2ac.png";
        Lang.ui.buttonVoteNegativeDisabled = "http://plug.dj/_/static/images/en/ButtonVoteNegativeDisabled.64485ab.png";
        Lang.ui.buttonAddThis = "http://plug.dj/_/static/images/en/ButtonAddThis.175d7d45.png";
        Lang.ui.buttonAddThisDisabled ="http://plug.dj/_/static/images/en/ButtonAddThisDisabled.b121845e.png";
        Lang.ui.buttonSkipThis = "http://plug.dj/_/static/images/en/ButtonSkipThis.b9a1c7b7.png";
        Lang.ui.buttonDJPlay = "http://plug.dj/_/static/images/en/ButtonDJPlay.742fd499.png";
        Lang.ui.buttonDJLeave = "http://plug.dj/_/static/images/en/ButtonDJQuit.1a691d0c.png";
        Lang.ui.buttonDJWaitlistJoin = "http://plug.dj/_/static/images/en/ButtonDJWaitListJoin.fbffc481.png";
        Lang.ui.buttonDJWaitlistLeave = "http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.5d5847b1.png";
        Lang.ui.buttonDJQuitShort = "http://plug.dj/_/static/images/en/ButtonDJQuitShort.8e572d1a.png";
        Lang.ui.buttonDJQuit = "http://plug.dj/_/static/images/en/ButtonDJQuit.1a691d0c.png";
        Lang.ui.buttonDJPlayShort = "http://plug.dj/_/static/images/en/ButtonDJPlayShort.b88f8f86.png";
        Lang.messages.fanEnter = "Seu fã %NAME% acabou de entrar na sala!"
        Lang.messages.fanOf = "Agora você é fã de %NAME%."
        Lang.messages.unFanOf = "Você não é mais fã de %NAME%."
        Lang.messages.follow = "%NAME% agora é seu fã!"
        Lang.messages.welcome = "Bem vindo ao plug.treta Version %VERSION%"
        Lang.messages.cap = "Limitando exibição de avatares á %COUNT%"
        Lang.rollover.becomeFan = "Virar Fã"
        Lang.rollover.fans = "fãs"
        Lang.rollover.host = "Anfitrião"
        Lang.alerts.updateMesage ="plug.dj has been updated and requires a refresh. Click OK to refresh the page."
        Lang.chat.help = "<strong>Chat Commands:</strong><br/>/em &nbsp; <em>Emote</em><br/>/me &nbsp; <em>Emote</em><br/>/clear &nbsp; <em>Clear Chat History</em><br/>/cap # &nbsp; <em>Limits the number of avatars rendered (1-200)</em><br/>/ts # &nbsp; <em>Chat timestamps (12, 24, 0)</em><br/>/emoji on (or off) <em>Enable/disable Emojis</em>"        
        API.off(API.CHAT,this.proxy.onChat)
        API.off(API.CHAT_COMMAND,this.customChatCommand)
        if(plugCubed != undefined) plugCubed.close();
        plugCubed = undefined
        if(plugBot != undefined) plugBot.close();
        plugBot = undefined
        if (this.socket) {
        this.socket.onclose = function() {};
        this.socket.close();
        }
    },
    initCSS: function() {
        $('#room-wheel').css('background','url("http://i.imgur.com/Zz8V7wd.png")');
        $('#room-wheel').css('background-repeat','no-repeat');
        $('#room-wheel').css('background-position','550px 275px');
        $('#meta-frame .frame-background').hide('.frame-background');
        $('#button-dj-waitlist-join').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png); display: block;');
        $('#button-dj-waitlist-leave').attr('style','background-image:url(http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png); display: block;');
        $('#button-dj-play').attr('style','background-image:url(http://plug.dj/_/static/images/pt/ButtonDJWaitListJoin.7d23a08.png); display: block;');
        $('#button-dj-leave').attr('style','background-image:url(http://plug.dj/_/static/images/pt/ButtonDJQuitShort.32e4f67.png); display: block;');
        $('#dj-console').attr('style','background-image:url(http://i.imgur.com/vdHvSaq.png); display:block; position:absolute; top:15px; width:317px;');
        $('#button-add-this').attr('style','background-image:url(http://plug.dj/_/static/images/pt/ButtonAddThis.b8afd7d.png);');
        $('#meta-frame').css('background-color','transparent');
        $('#playback .frame-background').hide('.frame-background');
        $('#playback').css('background-color','transparent');
        $('body').attr('style','background: none');
            $('head').append('<link href="http://fonts.googleapis.com/css?family=Faster+One" rel="stylesheet" type="text/css">'
            + '<style type="text/css" id="TFL-css">'
            + 'html{background: url("http://i.imgur.com/A43Okjz.jpg") no-repeat scroll center top #000000;}'
            + '#button-lobby { background-image: url("http://i.imgur.com/uXErh37.png");}'
            + 'body {color:#66FFFF;}'
            + '#current-dj-value {color:#66FFFF;}'
            + '.chat-title {font-family: "Faster One", cursive;}'
            + '#button-dj-play.button-dj {background-image: url("http://plug.dj/_/static/images/pt/ButtonDJWaitListJoin.7d23a08.png");}'
            + '#button-dj-quit.button-dj {background-image: url("http://plug.dj/_/static/images/en/ButtonDJWaitListLeave.340838e.png");}'
            + '#button-dj-waitlist-join.button-dj {background-image: url("http://i.imgur.com/UXxVIfm.png");}'
            + '#button-dj-waitlist-leave.button-dj {background-image: url("http://i.imgur.com/rZRTSu4.png");}'
            + '#button-dj-waitlist-view {background-image: url("http://plug.dj/_/static/images/pt/ButtonDJWaitListView.893548b.png");}'
            + '#button-my-playlists {background-image: url("http://plug.dj/_/static/images/pt/ButtonMyPlaylists.e01df22.png");}'
            + '#button-share-facebook {background-image: url("http://i.imgur.com/bEJHxvR.png");}'
            + '#button-share-twitter {background-image: url("http://i.imgur.com/NmM2mRY.png");}'
            + '#button-refresh {background-image: url("http://plug.dj/_/static/images/pt/ButtonRefresh.608485b.png");}'
            + '#button-hd-on {background-image: url("http://i.imgur.com/NY4Oytd.png");}'
            + '#button-hd-off {background-image: url("http://i.imgur.com/ZImzOjK.png");}'
            + '#current-dj-value {color:#66FFFF;}'
            + '#now-playing-value{color:#66FFFF;}'
            + '#room-score-value{color:#66FFFF;}'
            + '#chat {color:#00D1FF;}'
            + '.chat-cohost {color:#00FF95;}'
            + '.chat-host {color:#4CFF00;}'
            + '.chat-emote {color:#FCFF00;}'    
            + '.chat-emote .chat-from {color:#FCFF00;}'
            + '.chat-emote .chat-text, .chat-system .chat-text {color:FCFF00;}'
            + '.chat-host {background-image: url("http://i.imgur.com/aHUx8T9.png");}'
            + '.chat-cohost {background-image: url("http://i.imgur.com/VlkBKZ0.png");}'
            + '.chat-manager{background-image: url("https://dl.dropboxusercontent.com/u/198705975/radioative_icon.png");}'
            + '.chat-bouncer{background-image: url("http://i.imgur.com/t7pIDcb.png");}'
            + '.chat-from-featureddj {background: url("http://i.imgur.com/tlXvCWf.png") no-repeat;}'
            + '.chat-from-featureddj {padding-left:17px;}'
            + '.chat-message .chat-from-featureddj, .chat-mention .chat-from-featureddj {color:#3399FF !important;}'
            + '.chat-message .chat-from-bouncer, .chat-mention .chat-from-bouncer {color:#E90E82  !important;}'
            + '.chat-message .chat-from-manager, .chat-mention .chat-from-manager {color:#00EDT00!important;}'
            + '.chat-message .chat-from, .chat-mention .chat-from{background: url("http://i.imgur.com/9qWWO4L.png") no-repeat;}'
            + '.chat-message .chat-from, .chat-mention .chat-from {padding-left:17px;}'
            + '.chat-from-you {background: url("http://i.imgur.com/9qWWO4L.png") no-repeat;}'
            + '.chat-from-you {padding-left:17px;}'
            + '.chat-manager {color:#20F92E}'
            + '.chat-message .chat-from-host, .chat-mention .chat-from-host {color:#20F92E !important;}'
            + '.chat-message .chat-from-cohost, .chat-mention .chat-from-cohost {color:#EF00FF !important;}'
            + '.chat-moderation .chat-from {color:#00FF22;}'
            + '.chat-moderation {color:#F0F6F1;}'
            + '.chat-text a:link {color:#FCFF00;}'
            + '.chat-text a:visited {color:#22FF00;}'
            + '.chat-text a:hover {color:#EF00FF;}'
            + '.chat-text a:active {color:#66FFFF;}'
            + '#volume-bar-value {background-image: url("http://i.imgur.com/QQn379J.png");}'
        + '</style>');
},
initPopout : function(){
        var popout = require('app/views/room/popout/PopoutView');
        var css = document.createElement('style');
        css.type = 'text/css';
            var styles = 'body {color:#66FFFF}';
            styles+= '#current-dj-value {color:#F5FBFB}';
            styles+= '.chat-title {font-family: "Faster One", cursive}';
            styles+= '#current-dj-value {color:#F5FBFB}';
            styles+= '#now-playing-value{color:#F9FDFD}';
            styles+= '#room-score-value{color:#F8FDFD}';
            styles+= '#chat {color:#F1F7F8}';
            styles+= '.chat-cohost {color:#F1F8F5}';
            styles+= '.chat-host {color:#F9FBF8}';
            styles+= '.chat-emote {color:#FCFF00}';    
            styles+= '.chat-emote .chat-from {color:#FCFF00}';
            styles+= '.chat-emote .chat-text, .chat-system .chat-text {color:FCFF00}';
            styles+= '.chat-host {background-image: url("http://i.imgur.com/aHUx8T9.png")}';
            styles+= '.chat-cohost {background-image: url("http://i.imgur.com/VlkBKZ0.png")}';
            styles+= '.chat-manager {background-image: url("http://i.imgur.com/810HRng.png")}';
            styles+= '.chat-bouncer{background-image: url("http://i.imgur.com/t7pIDcb.png")}';
            styles+= '.chat-from-featureddj {background: url("http://i.imgur.com/D6pKyRJ.png") no-repeat}';
            styles+= '.chat-from-featureddj {padding-left:17px}';
            styles+= '.chat-message .chat-from-featureddj, .chat-mention .chat-from-featureddj {color:#F300FF !important}';
            styles+= '.chat-message .chat-from-bouncer, .chat-mention .chat-from-bouncer {color:#F300FF !important}';
            styles+= '.chat-message .chat-from-manager, .chat-mention .chat-from-manager {color:#E105F1 !important}';
            styles+= '.chat-message .chat-from, .chat-mention .chat-from{background: url("http://i.imgur.com/mmBNDrG.png") no-repeat}';
            styles+= '.chat-message .chat-from, .chat-mention .chat-from {padding-left:17px}';
            styles+= '.chat-from-you {background: url("http://i.imgur.com/HF5pnAR.png") no-repeat}';
            styles+= '.chat-from-you {padding-left:17px}';
            styles+= '.chat-manager {color:#20F92E}';
            styles+= '.chat-message .chat-from-host, .chat-mention .chat-from-host {color:#FF4000 !important}';
            styles+= '.chat-message .chat-from-cohost, .chat-mention .chat-from-cohost {color:#433E94 !important}';
            styles+= '.chat-moderation .chat-from {color:#F5FAF6}';
            styles+= '.chat-moderation {color:#FAFDFA}';
            styles+= '.chat-text a:link {color:#FCFF00}';
            styles+= '.chat-text a:visited {color:#F9FAF8}';
            styles+= '.chat-text a:hover {color:#EF00FF}';
            styles+= '.chat-text a:active {color:#FBFFFF}';
            styles+= '#volume-bar-value {background-image: url("http://i.imgur.com/QQn379J.png")}';
            if (css.styleSheet) css.styleSheet.cssText = styles;
            else css.appendChild(document.createTextNode(styles));
            popout._window.document.head.appendChild(css);
},
    onChat: function(data) {
        var  AudienceView = require ('app/views/room/AudienceView');
        if (data.type == 'message' && (API.hasPermission(data.fromID, API.ROLE.MANAGER)  || data.fromID == "50aeb077877b9217e2fbff00") && data.message.indexOf('!strobe on') === 0) {
            API.chatLog(data.from + ' hit the strobe light!');
           AudienceView.strobeMode('true');
        } else if (data.type == 'message' && (API.hasPermission(data.fromID, API.ROLE.MANAGER)|| data.fromID == "50aeb077877b9217e2fbff00") && data.message.indexOf('!strobe off') === 0) {
            AudienceView.strobeMode();
        } else if (data.type == 'message' && (API.hasPermission(data.fromID, API.ROLE.MANAGER)  || data.fromID == "50aeb077877b9217e2fbff00") && data.message.indexOf('!rave on') === 0) {
            API.chatLog(data.from + ' turned the lights down!');
             AudienceView.lightsOut('true');
        } else if (data.type == 'message' && (API.hasPermission(data.fromID, API.ROLE.MANAGER)  || data.fromID == "50aeb077877b9217e2fbff00") && data.message.indexOf('!rave off') === 0) {
            AudienceView.lightsOut();
        }
        if (data.fromID == '5194c32d96fba57f21243cc4')
        {
            $('.chat-manager').attr('style','background-image:url(http://i.imgur.com/hPQ6ghY.png);');
            $('.chat-manager').css('color','#AB00FF');
        }
        if (data.fromID === API.getUser().id && this.socket.readyState === SockJS.OPEN)
        this.socket.send(JSON.stringify({type:"chat",msg:data.message,chatID:data.chatID, username:data.from, ID:data.fromID, room:window.location.pathname.split('/')[1]}));
    },
    customChatCommand: function(value) {
         var  AudienceView = require ('app/views/room/AudienceView');
        if (value == '/strobe on'){API.chatLog(API.getUser().username +  ' hit the strobe light!'); AudienceView.strobeMode('true'), !0}
        if (value == '/strobe off'){AudienceView.strobeMode(),!0}
        if (value == '/rave on'){API.chatLog(API.getUser().username + ' turned the lights down!'); AudienceView.lightsOut('true'),!0}
        if (value == '/rave off'){AudienceView.lightsOut(),!0}
        if (value == '/close'){return TFLEnhanced.close(),!0}
        if (value.indexOf('/Avatar')=== 0){
            var i =value.substr(8);
            if(i >= 10)
                {
                var avatar = require('app/services/user/UserChangeAvatarService');
                 avatar = new avatar('halloween'+ i);
                };
            if(i<=9)
             {
                var avatar = require('app/services/user/UserChangeAvatarService');
                avatar = new avatar('halloween0'+ i);
             };
        }
       if (value == '/Auto On'){if(plugBot == undefined){$.getScript('https://raw.github.com/thedark1337/Plugbot/master/plugbot.js')}};
    },
    removeElements: function() {
        require('app/views/room/AudienceView').initRoomElements = function() {}
        require('app/views/room/AudienceView').defaultRoomElements = function(){}
        require('app/views/room/AudienceView').roomElements = []
        delete require('app/views/room/AudienceView').cactusHit
        delete require('app/views/room/AudienceView').cactus
        delete require('app/views/room/AudienceView').mountainHit
        delete require('app/views/room/AudienceView').mountain
        delete require('app/views/room/AudienceView').archHit
        delete require('app/views/room/AudienceView').arch
        delete require('app/views/room/AudienceView').cloudHit
        delete require('app/views/room/AudienceView').cloud
        require('app/base/Context').trigger('audience:redraw')
    },
 
    Socket: function(){
        this.socket = new SockJS('http://nonee.com');
        this.socket.tries = 0;
 
        this.socket.onopen =  function() {
            this.tries = 0;
            var userInfo = API.getUser();
            this.send(JSON.stringify({
                type:    'userinfo',
                id:       userInfo.id,
                username: userInfo.username,
                room:     window.location.pathname.split('/')[1],
                version:  TFLEnhanced.toString()
            }))
        }
       this.socket.onmessage = function(msg) {
        var data = JSON.parse(msg.data);
        if(data.type === 'update'){
            TFLEnhanced.socket.onclose = function (){};
            TFLEnhanced.socket.close();
            API.chatLog('new version of TFL Enhanced Released, Update in a few seconds');
            setTimeout(function() {$.getScript('https://raw.github.com/Colgate/TFL-Enhanced/master/TFLenhanced.js')},5000)
            return;
        }
       }
       this.socket.onclose = function() {
        this.tries++;
 
        var lag;
        if (this.tries <5)       lag =5;
        else if (this.tries <30) lag =30;
        else if (this.tries <60) lag =60;
        else                     return;
 
        setTimeout(function(){TFLEnhanced.Socket();},lag*1E3);
       }
    },
 
});
var TFLEnhanced = new TFLEnhancedModel;

/* Modified by Ebola ###
 *
 * - Features:
 * 1. added an emoticons dialog
 * 		- recent emoticons (me & users)
 * 		- catalog based on emoji cheat sheet
 *   	- press CTRL + mouse click to add emoticons continuously
 *   		(without dialog closing)
 *   	- smartly add spaces between emoticon text
 * 2. press arrow up/down in chat box to search chat history
 * 		- 1. make sure chat box is empty then press arrow UP
 * 		- 2. press UP/DOWN continuously to search between
 * 			older and newer messages
 * 		- 3. press other keys would stop searching immediately
 * 		- max 20 items
 * 3. press ESC to focus chat box (when chat box is not focused),
 * 		press ESC to clear chat box while typing (chat box is focused)
 * 4. added an AUTO-MEH button (just for fun, but srsly, don't press it!)
 * 5. added an OPEN VIDEO LINK button (without ?feature=player_embedded
 * 		in url if u wanna paste the link in social media,
 * 		soundcloud not supported)
 * 6. show user-box when clicking username in user-list
 * 7. fixed skipping video problem in original script (resume volume
 * 		and video in next track)
 * 8. improved browser performance when switching song (dj advances)
 * 9. improved browser performance when plug.dj tab is not focused
 * 10. suppress "This session has now ended. Goodbye." alert box
 * 		(still need to refresh the page when session dies)
 *
 * - Version:
 * 1.06.1
 *
 * - Latest changelog:
 * 1. Merged code from PlugBot v1.2
 * 2. Updates userlist when queue state changes
 *
 * - Issues:
 * Empty
 *
 * This script is on Github:
 * https://github.com/ebola777/Plugbot-Enhanced-by-Ebola
 *
 * 26 JULY 2013,
 * Ebola
 */

/*
 * This program is free software: you can redistribute it and/or modify
 * it under the terms of the GNU General Public License as published by
 * the Free Software Foundation, either version 3 of the License, or
 * (at your option) any later version.
 *
 * This program is distributed in the hope that it will be useful,
 * but WITHOUT ANY WARRANTY; without even the implied warranty of
 * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 * GNU General Public License for more details.
 *
 * You should have received a copy of the GNU General Public License
 * along with this program.  If not, see <http://www.gnu.org/licenses/>.
 */

/*
 * TERMS OF REPRODUCTION USE
 *
 * 1. Provide a link back to the original repository (this repository), as
 *     	in, https://github.com/ConnerGDavis/Plugbot, that is well-visible
 * 		wherever the source is being reproduced.  For example, should you
 * 		display it on a website, you should provide a link above/below that
 *		which the users use, titled something such as "ORIGINAL AUTHOR".
 *
 * 2. Retain these three comments:  the GNU GPL license statement, this comment,
 * 		and that below it, that details the author and purpose.
 *
 * Failure to follow these terms will result in me getting very angry at you
 * and having your software tweaked or removed if possible.  Either way, you're
 * still an idiot for not following such a basic rule, so at least I'll have
 * that going for me.
 */
var req=function(a,x){require([a],function(a){window[x]=a})};req("app/models/3rd/PlugBot","PlugBot");
define("app/models/3rd/EmojiUI",["jquery","app/base/Class","app/utils/Utilities","app/utils/Emoji"],function(a,x,B,C){return new (x.extend({init:function(){this.TIMEOUT_FADEDiALOG=1500;this.TAB_RECENTMe=0;this.TAB_RECENTUsERS=1;this.BLOCK_HEIGHT=this.BLOCK_WIDTH=17;this.SPRITE_WIDTH=135;this.SPRITE_HEIGHT=2022;this.SPRITE_SCALE=1.2;this.KEYCODE_CONTI=17;this.KEYCODE_ARROWUp=38;this.KEYCODE_ARROWDoWN=40;this.KEYCODE_ESC=27;this.MAX_RECENT={0:40,1:80};this.MAX_HISTORYChAT=20;this.conti=this.visible=
this.autoHide=!1;this.historyMessage=[];this.historyConti=!1;this.historyIndex=-1;this.recentItems={0:{},1:{}};this.timeout_fadeDialog=null;this.hasInitHandlers2=!1;this.dialog=null;this.scrollTop={};this.preventScroll=!1;this.currentTab=3;this.tabs=[{name:"Recent (Me)",index:0},{name:"Recent (Users)",index:1},{name:"All",index:2},{name:"Common",index:3},{name:"People",index:4},{name:"Nature",index:5},{name:"Objects",index:6},{name:"Places",index:7},{name:"Symbols",index:8}];this.rightItems={};this.cons=
{">:(":"angry",">XD":"astonished",":DX":"bowtie","</3":"broken_heart",":$":"confused",X$:"confounded",":~(":"cry",":[":"disappointed",":~[":"disappointed_relieved",XO:"dizzy_face",":|":"expressionless","8|":"flushed",":(":"frowning",":#":"grimacing",":D":"grinning","<3":"heart","<3)":"heart_eyes","O:)":"innocent",":~)":"joy",":*":"kissing",":<3":"kissing_heart","X<3":"kissing_closed_eyes",XD:"laughing",":O":"open_mouth","Z:|":"sleeping",":)":"smiley",":/":"smirk",T_T:"sob",":P":"stuck_out_tongue",
"X-P":"stuck_out_tongue_closed_eyes",";P":"stuck_out_tongue_winking_eye","B-)":"sunglasses","~:(":"sweat","~:)":"sweat_smile",XC:"tired_face",">:/":"unamused",";)":"wink"};r={100:"1f4af",1234:"1f522","-1":"1f44e","+1":"1f44d","8ball":"1f3b1",abcd:"1f521",abc:"1f524",ab:"1f18e",accept:"1f251",aerial_tramway:"1f6a1",airplane:"2708",alarm_clock:"23f0",alien:"1f47d",ambulance:"1f691",anchor:"2693",angel:"1f47c",anger:"1f4a2",angry:"1f620",anguished:"1f627",ant:"1f41c",a:"1f170",apple:"1f34e",aquarius:"2652",
aries:"2648",arrow_backward:"25c0",arrow_double_down:"23ec",arrow_double_up:"23eb",arrow_down:"2b07",arrow_down_small:"1f53d",arrow_forward:"25b6",arrow_heading_down:"2935",arrow_heading_up:"2934",arrow_left:"2b05",arrow_lower_left:"2199",arrow_lower_right:"2198",arrow_right_hook:"21aa",arrow_right:"27a1",arrows_clockwise:"1f503",arrows_counterclockwise:"1f504",arrow_up_down:"2195",arrow_upper_left:"2196",arrow_upper_right:"2197",arrow_up:"2b06",arrow_up_small:"1f53c",articulated_lorry:"1f69b",art:"1f3a8",
astonished:"1f632",athletic_shoe:"1f45f",atm:"1f3e7",baby_bottle:"1f37c",baby_chick:"1f424",baby:"1f476",baby_symbol:"1f6bc",back:"1f519",baggage_claim:"1f6c4",balloon:"1f388",ballot_box_with_check:"2611",bamboo:"1f38d",banana:"1f34c",bangbang:"203c",bank:"1f3e6",barber:"1f488",bar_chart:"1f4ca",baseball:"26be",basketball:"1f3c0",bath:"1f6c0",bathtub:"1f6c1",battery:"1f50b",bear:"1f43b",bee:"1f41d",beer:"1f37a",beers:"1f37b",beetle:"1f41e",beginner:"1f530",bell:"1f514",bento:"1f371",bicyclist:"1f6b4",
bike:"1f6b2",bikini:"1f459",bird:"1f426",birthday:"1f382",black_circle:"26ab",black_joker:"1f0cf",black_large_square:"2b1b",black_medium_small_square:"25fe",black_medium_square:"25fc",black_nib:"2712",black_small_square:"25aa",black_square_button:"1f532",blossom:"1f33c",blowfish:"1f421",blue_book:"1f4d8",blue_car:"1f699",blue_heart:"1f499",blush:"1f60a",boar:"1f417",boat:"26f5",bomb:"1f4a3",bookmark:"1f516",bookmark_tabs:"1f4d1",book:"1f4d6",books:"1f4da",boom:"1f4a5",boot:"1f462",bouquet:"1f490",
bowling:"1f3b3",bow:"1f647",bowtie:"bowtie",boy:"1f466",b:"1f171",bread:"1f35e",bride_with_veil:"1f470",bridge_at_night:"1f309",briefcase:"1f4bc",broken_heart:"1f494",bug:"1f41b",bulb:"1f4a1",bullettrain_front:"1f685",bullettrain_side:"1f684",bus:"1f68c",busstop:"1f68f",bust_in_silhouette:"1f464",busts_in_silhouette:"1f465",cactus:"1f335",cake:"1f370",calendar:"1f4c6",calling:"1f4f2",camel:"1f42b",camera:"1f4f7",cancer:"264b",candy:"1f36c",capital_abcd:"1f520",capricorn:"2651",card_index:"1f4c7",
carousel_horse:"1f3a0",car:"1f697",cat2:"1f408",cat:"1f431",cd:"1f4bf",chart:"1f4b9",chart_with_downwards_trend:"1f4c9",chart_with_upwards_trend:"1f4c8",checkered_flag:"1f3c1",cherries:"1f352",cherry_blossom:"1f338",chestnut:"1f330",chicken:"1f414",children_crossing:"1f6b8",chocolate_bar:"1f36b",christmas_tree:"1f384",church:"26ea",cinema:"1f3a6",circus_tent:"1f3aa",city_sunrise:"1f307",city_sunset:"1f306",clapper:"1f3ac",clap:"1f44f",clipboard:"1f4cb",clock1030:"1f565",clock10:"1f559",clock1130:"1f566",
clock11:"1f55a",clock1230:"1f567",clock12:"1f55b",clock130:"1f55c",clock1:"1f550",clock230:"1f55d",clock2:"1f551",clock330:"1f55e",clock3:"1f552",clock430:"1f55f",clock4:"1f553",clock530:"1f560",clock5:"1f554",clock630:"1f561",clock6:"1f555",clock730:"1f562",clock7:"1f556",clock830:"1f563",clock8:"1f557",clock930:"1f564",clock9:"1f558",closed_book:"1f4d5",closed_lock_with_key:"1f510",closed_umbrella:"1f302",cloud:"2601",cl:"1f191",clubs:"2663",cn:"1f1e8-1f1f3",cocktail:"1f378",coffee:"2615",cold_sweat:"1f630",
collision:"1f4a5",computer:"1f4bb",confetti_ball:"1f38a",confounded:"1f616",confused:"1f615",congratulations:"3297",construction:"1f6a7",construction_worker:"1f477",convenience_store:"1f3ea",cookie:"1f36a",cool:"1f192",cop:"1f46e",copyright:"00a9",corn:"1f33d",couplekiss:"1f48f",couple:"1f46b",couple_with_heart:"1f491",cow2:"1f404",cow:"1f42e",credit_card:"1f4b3",crescent_moon:"1f319",crocodile:"1f40a",crossed_flags:"1f38c",crown:"1f451",crying_cat_face:"1f63f",cry:"1f622",crystal_ball:"1f52e",cupid:"1f498",
curly_loop:"27b0",currency_exchange:"1f4b1",curry:"1f35b",custard:"1f36e",customs:"1f6c3",cyclone:"1f300",dancer:"1f483",dancers:"1f46f",dango:"1f361",dart:"1f3af",dash:"1f4a8",date:"1f4c5",deciduous_tree:"1f333",department_store:"1f3ec",de:"1f1e9-1f1ea",diamond_shape_with_a_dot_inside:"1f4a0",diamonds:"2666",disappointed:"1f61e",disappointed_relieved:"1f625",dizzy_face:"1f635",dizzy:"1f4ab",dog2:"1f415",dog:"1f436",dollar:"1f4b5",dolls:"1f38e",dolphin:"1f42c",do_not_litter:"1f6af",door:"1f6aa",doughnut:"1f369",
dragon_face:"1f432",dragon:"1f409",dress:"1f457",dromedary_camel:"1f42a",droplet:"1f4a7",dvd:"1f4c0",ear_of_rice:"1f33e",ear:"1f442",earth_africa:"1f30d",earth_americas:"1f30e",earth_asia:"1f30f",eggplant:"1f346",egg:"1f373",eight:"0038",eight_pointed_black_star:"2734",eight_spoked_asterisk:"2733",electric_plug:"1f50c",elephant:"1f418","e-mail":"1f4e7",email:"2709",end:"1f51a",envelope:"2709",envelope_with_arrow:"1f4e9",es:"1f1ea-1f1f8",european_castle:"1f3f0",european_post_office:"1f3e4",euro:"1f4b6",
evergreen_tree:"1f332",exclamation:"2757",expressionless:"1f611",eyeglasses:"1f453",eyes:"1f440",facepunch:"1f44a",factory:"1f3ed",fallen_leaf:"1f342",family:"1f46a",fast_forward:"23e9",fax:"1f4e0",fearful:"1f628",feelsgood:"feelsgood",feet:"1f43e",ferris_wheel:"1f3a1",file_folder:"1f4c1",finnadie:"finnadie",fire_engine:"1f692",fire:"1f525",fireworks:"1f386",first_quarter_moon:"1f313",first_quarter_moon_with_face:"1f31b",fish_cake:"1f365",fishing_pole_and_fish:"1f3a3",fish:"1f41f",fist:"270a",five:"0035",
flags:"1f38f",flashlight:"1f526",floppy_disk:"1f4be",flower_playing_cards:"1f3b4",flushed:"1f633",foggy:"1f301",football:"1f3c8",footprints:"1f463",fork_and_knife:"1f374",fountain:"26f2",four_leaf_clover:"1f340",four:"0034",free:"1f193",fried_shrimp:"1f364",fries:"1f35f",frog:"1f438",frowning:"1f626",fr:"1f1eb-1f1f7",fuelpump:"26fd",full_moon:"1f315",full_moon_with_face:"1f31d",game_die:"1f3b2",gb:"1f1ec-1f1e7",gemini:"264a",gem:"1f48e",ghost:"1f47b",gift_heart:"1f49d",gift:"1f381",girl:"1f467",globe_with_meridians:"1f310",
goat:"1f410",goberserk:"goberserk",godmode:"godmode",golf:"26f3",grapes:"1f347",green_apple:"1f34f",green_book:"1f4d7",green_heart:"1f49a",grey_exclamation:"2755",grey_question:"2754",grimacing:"1f62c",grinning:"1f600",grin:"1f601",guardsman:"1f482",guitar:"1f3b8",gun:"1f52b",haircut:"1f487",hamburger:"1f354",hammer:"1f528",hamster:"1f439",handbag:"1f45c",hand:"270b",hankey:"1f4a9",hash:"0023",hatched_chick:"1f425",hatching_chick:"1f423",headphones:"1f3a7",hear_no_evil:"1f649",heartbeat:"1f493",heart_decoration:"1f49f",
heart_eyes_cat:"1f63b",heart_eyes:"1f60d",heart:"2764",heartpulse:"1f497",hearts:"2665",heavy_check_mark:"2714",heavy_division_sign:"2797",heavy_dollar_sign:"1f4b2",heavy_exclamation_mark:"2757",heavy_minus_sign:"2796",heavy_multiplication_x:"2716",heavy_plus_sign:"2795",helicopter:"1f681",herb:"1f33f",hibiscus:"1f33a",high_brightness:"1f506",high_heel:"1f460",hocho:"1f52a",honeybee:"1f41d",honey_pot:"1f36f",horse:"1f434",horse_racing:"1f3c7",hospital:"1f3e5",hotel:"1f3e8",hotsprings:"2668",hourglass_flowing_sand:"23f3",
hourglass:"231b",house:"1f3e0",house_with_garden:"1f3e1",hurtrealbad:"hurtrealbad",hushed:"1f62f",ice_cream:"1f368",icecream:"1f366",ideograph_advantage:"1f250",id:"1f194",imp:"1f47f",inbox_tray:"1f4e5",incoming_envelope:"1f4e8",information_desk_person:"1f481",information_source:"2139",innocent:"1f607",interrobang:"2049",iphone:"1f4f1",it:"1f1ee-1f1f9",izakaya_lantern:"1f3ee",jack_o_lantern:"1f383",japanese_castle:"1f3ef",japanese_goblin:"1f47a",japanese_ogre:"1f479",japan:"1f5fe",jeans:"1f456",joy_cat:"1f639",
joy:"1f602",jp:"1f1ef-1f1f5",keycap_ten:"1f51f",key:"1f511",kimono:"1f458",kissing_cat:"1f63d",kissing_closed_eyes:"1f61a",kissing_heart:"1f618",kissing:"1f617",kissing_smiling_eyes:"1f619",kiss:"1f48b",koala:"1f428",koko:"1f201",kr:"1f1f0-1f1f7",lantern:"1f3ee",large_blue_circle:"1f535",large_blue_diamond:"1f537",large_orange_diamond:"1f536",last_quarter_moon:"1f317",last_quarter_moon_with_face:"1f31c",laughing:"1f606",leaves:"1f343",ledger:"1f4d2",left_luggage:"1f6c5",left_right_arrow:"2194",leftwards_arrow_with_hook:"21a9",
lemon:"1f34b",leopard:"1f406",leo:"264c",libra:"264e",light_rail:"1f688",link:"1f517",lips:"1f444",lipstick:"1f484",lock:"1f512",lock_with_ink_pen:"1f50f",lollipop:"1f36d",loop:"27bf",loudspeaker:"1f4e2",love_hotel:"1f3e9",love_letter:"1f48c",low_brightness:"1f505",mag:"1f50d",mag_right:"1f50e",mahjong:"1f004",mailbox_closed:"1f4ea",mailbox:"1f4eb",mailbox_with_mail:"1f4ec",mailbox_with_no_mail:"1f4ed",man:"1f468",mans_shoe:"1f45e",man_with_gua_pi_mao:"1f472",man_with_turban:"1f473",maple_leaf:"1f341",
mask:"1f637",massage:"1f486",meat_on_bone:"1f356",mega:"1f4e3",melon:"1f348",memo:"1f4dd",mens:"1f6b9",metal:"metal",metro:"1f687",microphone:"1f3a4",microscope:"1f52c",milky_way:"1f30c",minibus:"1f690",minidisc:"1f4bd",mobile_phone_off:"1f4f4",moneybag:"1f4b0",money_with_wings:"1f4b8",monkey_face:"1f435",monkey:"1f412",monorail:"1f69d",moon:"1f314",mortar_board:"1f393",mountain_bicyclist:"1f6b5",mountain_cableway:"1f6a0",mountain_railway:"1f69e",mount_fuji:"1f5fb",mouse2:"1f401",mouse:"1f42d",movie_camera:"1f3a5",
moyai:"1f5ff",m:"24c2",muscle:"1f4aa",mushroom:"1f344",musical_keyboard:"1f3b9",musical_note:"1f3b5",musical_score:"1f3bc",mute:"1f507",nail_care:"1f485",name_badge:"1f4db",neckbeard:"neckbeard",necktie:"1f454",negative_squared_cross_mark:"274e",neutral_face:"1f610",new_moon:"1f311",new_moon_with_face:"1f31a","new":"1f195",newspaper:"1f4f0",ng:"1f196",nine:"0039",no_bell:"1f515",no_bicycles:"1f6b3",no_entry:"26d4",no_entry_sign:"1f6ab",no_good:"1f645",no_mobile_phones:"1f4f5",no_mouth:"1f636","non-potable_water":"1f6b1",
no_pedestrians:"1f6b7",nose:"1f443",no_smoking:"1f6ad",notebook:"1f4d3",notebook_with_decorative_cover:"1f4d4",notes:"1f3b6",nut_and_bolt:"1f529",o2:"1f17e",ocean:"1f30a",octocat:"octocat",octopus:"1f419",oden:"1f362",office:"1f3e2",ok_hand:"1f44c",ok:"1f197",ok_woman:"1f646",older_man:"1f474",older_woman:"1f475",oncoming_automobile:"1f698",oncoming_bus:"1f68d",oncoming_police_car:"1f694",oncoming_taxi:"1f696",one:"0031",on:"1f51b",open_book:"1f4d6",open_file_folder:"1f4c2",open_hands:"1f450",open_mouth:"1f62e",
ophiuchus:"26ce",o:"2b55",orange_book:"1f4d9",outbox_tray:"1f4e4",ox:"1f402","package":"1f4e6",page_facing_up:"1f4c4",pager:"1f4df",page_with_curl:"1f4c3",palm_tree:"1f334",panda_face:"1f43c",paperclip:"1f4ce",parking:"1f17f",part_alternation_mark:"303d",partly_sunny:"26c5",passport_control:"1f6c2",paw_prints:"1f43e",peach:"1f351",pear:"1f350",pencil2:"270f",pencil:"1f4dd",penguin:"1f427",pensive:"1f614",performing_arts:"1f3ad",persevere:"1f623",person_frowning:"1f64d",person_with_blond_hair:"1f471",
person_with_pouting_face:"1f64e",phone:"260e",pig2:"1f416",pig_nose:"1f43d",pig:"1f437",pill:"1f48a",pineapple:"1f34d",pisces:"2653",pizza:"1f355",point_down:"1f447",point_left:"1f448",point_right:"1f449",point_up_2:"1f446",point_up:"261d",police_car:"1f693",poodle:"1f429",poop:"1f4a9",postal_horn:"1f4ef",postbox:"1f4ee",post_office:"1f3e3",potable_water:"1f6b0",pouch:"1f45d",poultry_leg:"1f357",pound:"1f4b7",pouting_cat:"1f63e",pray:"1f64f",princess:"1f478",punch:"1f44a",purple_heart:"1f49c",purse:"1f45b",
pushpin:"1f4cc",put_litter_in_its_place:"1f6ae",question:"2753",rabbit2:"1f407",rabbit:"1f430",racehorse:"1f40e",radio_button:"1f518",radio:"1f4fb",rage1:"rage1",rage2:"rage2",rage3:"rage3",rage4:"rage4",rage:"1f621",railway_car:"1f683",rainbow:"1f308",raised_hand:"1f64b",raised_hands:"1f64c",raising_hand:"1f64b",ramen:"1f35c",ram:"1f40f",rat:"1f400",recycle:"267b",red_car:"1f697",red_circle:"1f534",registered:"00ae",relaxed:"263a",relieved:"1f60c",repeat_one:"1f502",repeat:"1f501",restroom:"1f6bb",
revolving_hearts:"1f49e",rewind:"23ea",ribbon:"1f380",rice_ball:"1f359",rice_cracker:"1f358",rice:"1f35a",rice_scene:"1f391",ring:"1f48d",rocket:"1f680",roller_coaster:"1f3a2",rooster:"1f413",rose:"1f339",rotating_light:"1f6a8",round_pushpin:"1f4cd",rowboat:"1f6a3",rugby_football:"1f3c9",runner:"1f3c3",running:"1f3c3",running_shirt_with_sash:"1f3bd",ru:"1f1f7-1f1fa",sagittarius:"2650",sailboat:"26f5",sake:"1f376",sandal:"1f461",santa:"1f385",sa:"1f202",satellite:"1f4e1",satisfied:"1f606",saxophone:"1f3b7",
school:"1f3eb",school_satchel:"1f392",scissors:"2702",scorpius:"264f",scream_cat:"1f640",scream:"1f631",scroll:"1f4dc",seat:"1f4ba",secret:"3299",seedling:"1f331",see_no_evil:"1f648",seven:"0037",shaved_ice:"1f367",sheep:"1f411",shell:"1f41a",shipit:"shipit",ship:"1f6a2",shirt:"1f455",shit:"1f4a9",shoe:"1f45e",shower:"1f6bf",signal_strength:"1f4f6",six:"0036",six_pointed_star:"1f52f",ski:"1f3bf",skull:"1f480",sleeping:"1f634",sleepy:"1f62a",slot_machine:"1f3b0",small_blue_diamond:"1f539",small_orange_diamond:"1f538",
small_red_triangle_down:"1f53b",small_red_triangle:"1f53a",smile_cat:"1f638",smile:"1f604",smiley_cat:"1f63a",smiley:"1f603",smiling_imp:"1f608",smirk_cat:"1f63c",smirk:"1f60f",smoking:"1f6ac",snail:"1f40c",snake:"1f40d",snowboarder:"1f3c2",snowflake:"2744",snowman:"26c4",sob:"1f62d",soccer:"26bd",soon:"1f51c",sos:"1f198",sound:"1f509",space_invader:"1f47e",spades:"2660",spaghetti:"1f35d",sparkle:"2747",sparkler:"1f387",sparkles:"2728",sparkling_heart:"1f496",speaker:"1f50a",speak_no_evil:"1f64a",
speech_balloon:"1f4ac",speedboat:"1f6a4",squirrel:"squirrel",star2:"1f31f",star:"2b50",stars:"1f303",station:"1f689",statue_of_liberty:"1f5fd",steam_locomotive:"1f682",stew:"1f372",straight_ruler:"1f4cf",strawberry:"1f353",stuck_out_tongue_closed_eyes:"1f61d",stuck_out_tongue:"1f61b",stuck_out_tongue_winking_eye:"1f61c",sunflower:"1f33b",sunglasses:"1f60e",sunny:"2600",sunrise_over_mountains:"1f304",sunrise:"1f305",sun_with_face:"1f31e",surfer:"1f3c4",sushi:"1f363",suspect:"suspect",suspension_railway:"1f69f",
sweat_drops:"1f4a6",sweat:"1f613",sweat_smile:"1f605",sweet_potato:"1f360",swimmer:"1f3ca",symbols:"1f523",syringe:"1f489",tada:"1f389",tanabata_tree:"1f38b",tangerine:"1f34a",taurus:"2649",taxi:"1f695",tea:"1f375",telephone:"260e",telephone_receiver:"1f4de",telescope:"1f52d",tennis:"1f3be",tent:"26fa",thought_balloon:"1f4ad",three:"0033",thumbsdown:"1f44e",thumbsup:"1f44d",ticket:"1f3ab",tiger2:"1f405",tiger:"1f42f",tired_face:"1f62b",tm:"2122",toilet:"1f6bd",tokyo_tower:"1f5fc",tomato:"1f345",tongue:"1f445",
tophat:"1f3a9",top:"1f51d",tractor:"1f69c",traffic_light:"1f6a5",train2:"1f686",train:"1f683",tram:"1f68a",triangular_flag_on_post:"1f6a9",triangular_ruler:"1f4d0",trident:"1f531",triumph:"1f624",trolleybus:"1f68e",trollface:"trollface",trophy:"1f3c6",tropical_drink:"1f379",tropical_fish:"1f420",truck:"1f69a",trumpet:"1f3ba",tshirt:"1f455",tulip:"1f337",turtle:"1f422",tv:"1f4fa",twisted_rightwards_arrows:"1f500",two_hearts:"1f495",two_men_holding_hands:"1f46c",two:"0032",two_women_holding_hands:"1f46d",
u5272:"1f239",u5408:"1f234",u55b6:"1f23a",u6307:"1f22f",u6708:"1f237",u6709:"1f236",u6e80:"1f235",u7121:"1f21a",u7533:"1f238",u7981:"1f232",u7a7a:"1f233",uk:"1f1ec-1f1e7",umbrella:"2614",unamused:"1f612",underage:"1f51e",unlock:"1f513",up:"1f199",us:"1f1fa-1f1f8",vertical_traffic_light:"1f6a6",vhs:"1f4fc",vibration_mode:"1f4f3",video_camera:"1f4f9",video_game:"1f3ae",violin:"1f3bb",virgo:"264d",volcano:"1f30b",v:"270c",vs:"1f19a",walking:"1f6b6",waning_crescent_moon:"1f318",waning_gibbous_moon:"1f316",
warning:"26a0",watch:"231a",water_buffalo:"1f403",watermelon:"1f349",wave:"1f44b",wavy_dash:"3030",waxing_crescent_moon:"1f312",waxing_gibbous_moon:"1f314",wc:"1f6be",weary:"1f629",wedding:"1f492",whale2:"1f40b",whale:"1f433",wheelchair:"267f",white_check_mark:"2705",white_circle:"26aa",white_flower:"1f4ae",white_large_square:"2b1c",white_medium_small_square:"25fd",white_medium_square:"25fb",white_small_square:"25ab",white_square_button:"1f533",wind_chime:"1f390",wine_glass:"1f377",wink:"1f609",wolf:"1f43a",
woman:"1f469",womans_clothes:"1f45a",womans_hat:"1f452",womens:"1f6ba",worried:"1f61f",wrench:"1f527",x:"274c",yellow_heart:"1f49b",yen:"1f4b4",yum:"1f60b",zap:"26a1",zero:"0030",zzz:"1f4a4"};this.emo={0:[],1:[],2:":hash: :zero: :one: :two: :three: :four: :five: :six: :seven: :eight: :nine: :copyright: :registered: :mahjong: :black_joker: :a: :b: :o2: :parking: :ab: :cl: :cool: :free: :id: :new: :ng: :ok: :sos: :up: :vs: :cn: :de: :es: :fr: :uk: :it: :jp: :kr: :ru: :us: :koko: :sa: :u7121: :u6307: :u7981: :u7a7a: :u5408: :u6e80: :u6709: :u6708: :u7533: :u5272: :u55b6: :ideograph_advantage: :accept: :cyclone: :foggy: :closed_umbrella: :stars: :sunrise_over_mountains: :sunrise: :city_sunset: :city_sunrise: :rainbow: :bridge_at_night: :ocean: :volcano: :milky_way: :earth_africa: :earth_americas: :earth_asia: :globe_with_meridians: :new_moon: :waxing_crescent_moon: :first_quarter_moon: :waxing_gibbous_moon: :full_moon: :waning_gibbous_moon: :last_quarter_moon: :waning_crescent_moon: :crescent_moon: :new_moon_with_face: :first_quarter_moon_with_face: :last_quarter_moon_with_face: :full_moon_with_face: :sun_with_face: :star2: :chestnut: :seedling: :evergreen_tree: :deciduous_tree: :palm_tree: :cactus: :tulip: :cherry_blossom: :rose: :hibiscus: :sunflower: :blossom: :corn: :ear_of_rice: :herb: :four_leaf_clover: :maple_leaf: :fallen_leaf: :leaves: :mushroom: :tomato: :eggplant: :grapes: :melon: :watermelon: :tangerine: :lemon: :banana: :pineapple: :apple: :green_apple: :pear: :peach: :cherries: :strawberry: :hamburger: :pizza: :meat_on_bone: :poultry_leg: :rice_cracker: :rice_ball: :rice: :curry: :ramen: :spaghetti: :bread: :fries: :sweet_potato: :dango: :oden: :sushi: :fried_shrimp: :fish_cake: :icecream: :shaved_ice: :ice_cream: :doughnut: :cookie: :chocolate_bar: :candy: :lollipop: :custard: :honey_pot: :cake: :bento: :stew: :egg: :fork_and_knife: :tea: :sake: :wine_glass: :cocktail: :tropical_drink: :beer: :beers: :baby_bottle: :ribbon: :gift: :birthday: :jack_o_lantern: :christmas_tree: :santa: :fireworks: :sparkler: :balloon: :tada: :confetti_ball: :tanabata_tree: :crossed_flags: :bamboo: :dolls: :flags: :wind_chime: :rice_scene: :school_satchel: :mortar_board: :carousel_horse: :ferris_wheel: :roller_coaster: :fishing_pole_and_fish: :microphone: :movie_camera: :cinema: :headphones: :art: :tophat: :circus_tent: :ticket: :clapper: :performing_arts: :video_game: :dart: :slot_machine: :8ball: :game_die: :bowling: :flower_playing_cards: :musical_note: :notes: :saxophone: :guitar: :musical_keyboard: :trumpet: :violin: :musical_score: :running_shirt_with_sash: :tennis: :ski: :basketball: :checkered_flag: :snowboarder: :running: :surfer: :trophy: :horse_racing: :football: :rugby_football: :swimmer: :house: :house_with_garden: :office: :post_office: :european_post_office: :hospital: :bank: :atm: :hotel: :love_hotel: :convenience_store: :school: :department_store: :factory: :lantern: :japanese_castle: :european_castle: :rat: :mouse2: :ox: :water_buffalo: :cow2: :tiger2: :leopard: :rabbit2: :cat2: :dragon: :crocodile: :whale2: :snail: :snake: :racehorse: :ram: :goat: :sheep: :monkey: :rooster: :chicken: :dog2: :pig2: :boar: :elephant: :octopus: :shell: :bug: :ant: :honeybee: :beetle: :fish: :tropical_fish: :blowfish: :turtle: :hatching_chick: :baby_chick: :hatched_chick: :bird: :penguin: :koala: :poodle: :dromedary_camel: :camel: :dolphin: :mouse: :cow: :tiger: :rabbit: :cat: :dragon_face: :whale: :horse: :monkey_face: :dog: :pig: :frog: :hamster: :wolf: :bear: :panda_face: :pig_nose: :paw_prints: :eyes: :ear: :nose: :lips: :tongue: :point_up_2: :point_down: :point_left: :point_right: :punch: :wave: :ok_hand: :thumbsup: :thumbsdown: :clap: :open_hands: :crown: :womans_hat: :eyeglasses: :necktie: :tshirt: :jeans: :dress: :kimono: :bikini: :womans_clothes: :purse: :handbag: :pouch: :shoe: :athletic_shoe: :high_heel: :sandal: :boot: :footprints: :bust_in_silhouette: :busts_in_silhouette: :boy: :girl: :man: :woman: :family: :couple: :two_men_holding_hands: :two_women_holding_hands: :cop: :dancers: :bride_with_veil: :person_with_blond_hair: :man_with_gua_pi_mao: :man_with_turban: :older_man: :older_woman: :baby: :construction_worker: :princess: :japanese_ogre: :japanese_goblin: :ghost: :angel: :alien: :space_invader: :imp: :skull: :information_desk_person: :guardsman: :dancer: :lipstick: :nail_care: :massage: :haircut: :barber: :syringe: :pill: :kiss: :love_letter: :ring: :gem: :couplekiss: :bouquet: :couple_with_heart: :wedding: :heartbeat: </3 :two_hearts: :sparkling_heart: :heartpulse: :cupid: :blue_heart: :green_heart: :yellow_heart: :purple_heart: :gift_heart: :revolving_hearts: :heart_decoration: :diamond_shape_with_a_dot_inside: :bulb: :anger: :bomb: :zzz: :collision: :sweat_drops: :droplet: :dash: :shit: :muscle: :dizzy: :speech_balloon: :thought_balloon: :white_flower: :100: :moneybag: :currency_exchange: :heavy_dollar_sign: :credit_card: :yen: :dollar: :euro: :pound: :money_with_wings: :chart: :seat: :computer: :briefcase: :minidisc: :floppy_disk: :cd: :dvd: :file_folder: :open_file_folder: :page_with_curl: :page_facing_up: :date: :calendar: :card_index: :chart_with_upwards_trend: :chart_with_downwards_trend: :bar_chart: :clipboard: :pushpin: :round_pushpin: :paperclip: :straight_ruler: :triangular_ruler: :bookmark_tabs: :ledger: :notebook: :notebook_with_decorative_cover: :closed_book: :open_book: :green_book: :blue_book: :orange_book: :books: :name_badge: :scroll: :pencil: :telephone_receiver: :pager: :fax: :satellite: :loudspeaker: :mega: :outbox_tray: :inbox_tray: :package: :e-mail: :incoming_envelope: :envelope_with_arrow: :mailbox_closed: :mailbox: :mailbox_with_mail: :mailbox_with_no_mail: :postbox: :postal_horn: :newspaper: :iphone: :calling: :vibration_mode: :mobile_phone_off: :no_mobile_phones: :signal_strength: :camera: :video_camera: :tv: :radio: :vhs: :twisted_rightwards_arrows: :repeat: :repeat_one: :arrows_clockwise: :arrows_counterclockwise: :low_brightness: :high_brightness: :mute: :sound: :speaker: :battery: :electric_plug: :mag: :mag_right: :lock_with_ink_pen: :closed_lock_with_key: :key: :lock: :unlock: :bell: :no_bell: :bookmark: :link: :radio_button: :back: :end: :on: :soon: :top: :underage: :keycap_ten: :capital_abcd: :abcd: :1234: :symbols: :abc: :fire: :flashlight: :wrench: :hammer: :nut_and_bolt: :hocho: :gun: :microscope: :telescope: :crystal_ball: :six_pointed_star: :beginner: :trident: :black_square_button: :white_square_button: :red_circle: :large_blue_circle: :large_orange_diamond: :large_blue_diamond: :small_orange_diamond: :small_blue_diamond: :small_red_triangle: :small_red_triangle_down: :arrow_up_small: :arrow_down_small: :clock1: :clock2: :clock3: :clock4: :clock5: :clock6: :clock7: :clock8: :clock9: :clock10: :clock11: :clock12: :clock130: :clock230: :clock330: :clock430: :clock530: :clock630: :clock730: :clock830: :clock930: :clock1030: :clock1130: :clock1230: :mount_fuji: :tokyo_tower: :statue_of_liberty: :japan: :moyai: :D :grin: :~) :) :smile: ~:) :satisfied: O:) :smiling_imp: ;) :blush: :yum: :relieved: <3) B-) :/ :neutral_face: :| >:/ ~:( :pensive: :$ X$ :* :<3 :kissing_smiling_eyes: X<3 :P ;P X-P :[ :worried: >:( :rage: :~( :persevere: :triumph: :~[ :( :anguished: :fearful: :weary: :sleepy: XC :# T_T :O :hushed: :cold_sweat: :scream: >XD 8| Z:| XO :no_mouth: :mask: :smile_cat: :joy_cat: :smiley_cat: :heart_eyes_cat: :smirk_cat: :kissing_cat: :pouting_cat: :crying_cat_face: :scream_cat: :no_good: :ok_woman: :bow: :see_no_evil: :hear_no_evil: :speak_no_evil: :raising_hand: :raised_hands: :person_frowning: :person_with_pouting_face: :pray: :rocket: :helicopter: :steam_locomotive: :train: :bullettrain_side: :bullettrain_front: :train2: :metro: :light_rail: :station: :tram: :bus: :oncoming_bus: :trolleybus: :busstop: :minibus: :ambulance: :fire_engine: :police_car: :oncoming_police_car: :taxi: :oncoming_taxi: :red_car: :oncoming_automobile: :blue_car: :truck: :articulated_lorry: :tractor: :monorail: :mountain_railway: :suspension_railway: :mountain_cableway: :aerial_tramway: :ship: :rowboat: :speedboat: :traffic_light: :vertical_traffic_light: :construction: :rotating_light: :triangular_flag_on_post: :door: :no_entry_sign: :smoking: :no_smoking: :put_litter_in_its_place: :do_not_litter: :potable_water: :non-potable_water: :bike: :no_bicycles: :bicyclist: :mountain_bicyclist: :walking: :no_pedestrians: :children_crossing: :mens: :womens: :restroom: :baby_symbol: :toilet: :wc: :shower: :bath: :bathtub: :passport_control: :customs: :baggage_claim: :left_luggage: :bangbang: :interrobang: :tm: :information_source: :left_right_arrow: :arrow_up_down: :arrow_upper_left: :arrow_upper_right: :arrow_lower_right: :arrow_lower_left: :leftwards_arrow_with_hook: :arrow_right_hook: :watch: :hourglass: :fast_forward: :rewind: :arrow_double_up: :arrow_double_down: :alarm_clock: :hourglass_flowing_sand: :m: :black_small_square: :white_small_square: :arrow_forward: :arrow_backward: :white_medium_square: :black_medium_square: :white_medium_small_square: :black_medium_small_square: :sunny: :cloud: :telephone: :ballot_box_with_check: :umbrella: :coffee: :point_up: :relaxed: :aries: :taurus: :gemini: :cancer: :leo: :virgo: :libra: :scorpius: :sagittarius: :capricorn: :aquarius: :pisces: :spades: :clubs: :hearts: :diamonds: :hotsprings: :recycle: :wheelchair: :anchor: :warning: :zap: :white_circle: :black_circle: :soccer: :baseball: :snowman: :partly_sunny: :ophiuchus: :no_entry: :church: :fountain: :golf: :sailboat: :tent: :fuelpump: :scissors: :white_check_mark: :airplane: :envelope: :fist: :hand: :v: :pencil2: :black_nib: :heavy_check_mark: :heavy_multiplication_x: :sparkles: :eight_spoked_asterisk: :eight_pointed_black_star: :snowflake: :sparkle: :x: :negative_squared_cross_mark: :question: :grey_question: :grey_exclamation: :heavy_exclamation_mark: <3 :heavy_plus_sign: :heavy_minus_sign: :heavy_division_sign: :arrow_right: :curly_loop: :loop: :arrow_heading_up: :arrow_heading_down: :arrow_left: :arrow_up: :arrow_down: :black_large_square: :white_large_square: :star: :o: :wavy_dash: :part_alternation_mark: :congratulations: :secret: :DX :feelsgood: :finnadie: :goberserk: :godmode: :hurtrealbad: :metal: :neckbeard: :octocat: :rage1: :rage2: :rage3: :rage4: :shipit: :squirrel: :suspect: :trollface:".split(" "),
3:">:( >XD :DX :$ X$ :~( :[ :~[ XO :| 8| :( :# :D <3) O:) :~) :* :<3 X<3 XD :O Z:| :) :/ T_T :P X-P ;P B-) ~:( ~:) XC >:/ ;) </3 <3 :blue_heart: :green_heart: :yellow_heart: :purple_heart: :kiss: :trollface: :shit: :thumbsup: :thumbsdown: :v: :metal:".split(" "),4:":DX :smile: XD :blush: :) :relaxed: :/ <3) :<3 X<3 8| :relieved: :satisfied: :grin: ;) ;P X-P :D :* :kissing_smiling_eyes: :P Z:| :worried: :( :anguished: :O :# :$ :hushed: :| >:/ ~:) ~:( :~[ :weary: :pensive: :[ X$ :fearful: :cold_sweat: :persevere: :~( T_T :~) >XD :scream: :neckbeard: XC >:( :rage: :triumph: :sleepy: :yum: :mask: B-) XO :imp: :smiling_imp: :neutral_face: :no_mouth: O:) :alien: :yellow_heart: :blue_heart: :purple_heart: <3 :green_heart: </3 :heartbeat: :heartpulse: :two_hearts: :revolving_hearts: :cupid: :sparkling_heart: :sparkles: :star: :star2: :dizzy: :boom: :collision: :anger: :exclamation: :question: :grey_exclamation: :grey_question: :zzz: :dash: :sweat_drops: :notes: :musical_note: :fire: :hankey: :poop: :shit: :+1: :thumbsup: :-1: :thumbsdown: :ok_hand: :punch: :facepunch: :fist: :v: :wave: :hand: :raised_hand: :open_hands: :point_up: :point_down: :point_left: :point_right: :raised_hands: :pray: :point_up_2: :clap: :muscle: :metal: :walking: :runner: :running: :couple: :family: :two_men_holding_hands: :two_women_holding_hands: :dancer: :dancers: :ok_woman: :no_good: :information_desk_person: :raising_hand: :bride_with_veil: :person_with_pouting_face: :person_frowning: :bow: :couplekiss: :couple_with_heart: :massage: :haircut: :nail_care: :boy: :girl: :woman: :man: :baby: :older_woman: :older_man: :person_with_blond_hair: :man_with_gua_pi_mao: :man_with_turban: :construction_worker: :cop: :angel: :princess: :smiley_cat: :smile_cat: :heart_eyes_cat: :kissing_cat: :smirk_cat: :scream_cat: :crying_cat_face: :joy_cat: :pouting_cat: :japanese_ogre: :japanese_goblin: :see_no_evil: :hear_no_evil: :speak_no_evil: :guardsman: :skull: :feet: :lips: :kiss: :droplet: :ear: :eyes: :nose: :tongue: :love_letter: :bust_in_silhouette: :busts_in_silhouette: :speech_balloon: :thought_balloon: :feelsgood: :finnadie: :goberserk: :godmode: :hurtrealbad: :rage1: :rage2: :rage3: :rage4: :suspect: :trollface:".split(" "),
5:":sunny: :umbrella: :cloud: :snowflake: :snowman: :zap: :cyclone: :foggy: :ocean: :cat: :dog: :mouse: :hamster: :rabbit: :wolf: :frog: :tiger: :koala: :bear: :pig: :pig_nose: :cow: :boar: :monkey_face: :monkey: :horse: :racehorse: :camel: :sheep: :elephant: :panda_face: :snake: :bird: :baby_chick: :hatched_chick: :hatching_chick: :chicken: :penguin: :turtle: :bug: :honeybee: :ant: :beetle: :snail: :octopus: :tropical_fish: :fish: :whale: :whale2: :dolphin: :cow2: :ram: :rat: :water_buffalo: :tiger2: :rabbit2: :dragon: :goat: :rooster: :dog2: :pig2: :mouse2: :ox: :dragon_face: :blowfish: :crocodile: :dromedary_camel: :leopard: :cat2: :poodle: :paw_prints: :bouquet: :cherry_blossom: :tulip: :four_leaf_clover: :rose: :sunflower: :hibiscus: :maple_leaf: :leaves: :fallen_leaf: :herb: :mushroom: :cactus: :palm_tree: :evergreen_tree: :deciduous_tree: :chestnut: :seedling: :blossom: :ear_of_rice: :shell: :globe_with_meridians: :sun_with_face: :full_moon_with_face: :new_moon_with_face: :new_moon: :waxing_crescent_moon: :first_quarter_moon: :waxing_gibbous_moon: :full_moon: :waning_gibbous_moon: :last_quarter_moon: :waning_crescent_moon: :last_quarter_moon_with_face: :first_quarter_moon_with_face: :moon: :earth_africa: :earth_americas: :earth_asia: :volcano: :milky_way: :partly_sunny: :octocat: :squirrel:".split(" "),
6:":bamboo: :gift_heart: :dolls: :school_satchel: :mortar_board: :flags: :fireworks: :sparkler: :wind_chime: :rice_scene: :jack_o_lantern: :ghost: :santa: :christmas_tree: :gift: :bell: :no_bell: :tanabata_tree: :tada: :confetti_ball: :balloon: :crystal_ball: :cd: :dvd: :floppy_disk: :camera: :video_camera: :movie_camera: :computer: :tv: :iphone: :phone: :telephone: :telephone_receiver: :pager: :fax: :minidisc: :vhs: :sound: :speaker: :mute: :loudspeaker: :mega: :hourglass: :hourglass_flowing_sand: :alarm_clock: :watch: :radio: :satellite: :loop: :mag: :mag_right: :unlock: :lock: :lock_with_ink_pen: :closed_lock_with_key: :key: :bulb: :flashlight: :high_brightness: :low_brightness: :electric_plug: :battery: :calling: :email: :mailbox: :postbox: :bath: :bathtub: :shower: :toilet: :wrench: :nut_and_bolt: :hammer: :seat: :moneybag: :yen: :dollar: :pound: :euro: :credit_card: :money_with_wings: :e-mail: :inbox_tray: :outbox_tray: :envelope: :incoming_envelope: :postal_horn: :mailbox_closed: :mailbox_with_mail: :mailbox_with_no_mail: :door: :smoking: :bomb: :gun: :hocho: :pill: :syringe: :page_facing_up: :page_with_curl: :bookmark_tabs: :bar_chart: :chart_with_upwards_trend: :chart_with_downwards_trend: :scroll: :clipboard: :calendar: :date: :card_index: :file_folder: :open_file_folder: :scissors: :pushpin: :paperclip: :black_nib: :pencil2: :straight_ruler: :triangular_ruler: :closed_book: :green_book: :blue_book: :orange_book: :notebook: :notebook_with_decorative_cover: :ledger: :books: :bookmark: :name_badge: :microscope: :telescope: :newspaper: :football: :basketball: :soccer: :baseball: :tennis: :8ball: :rugby_football: :bowling: :golf: :mountain_bicyclist: :bicyclist: :horse_racing: :snowboarder: :swimmer: :surfer: :ski: :spades: :hearts: :clubs: :diamonds: :gem: :ring: :trophy: :musical_score: :musical_keyboard: :violin: :space_invader: :video_game: :black_joker: :flower_playing_cards: :game_die: :dart: :mahjong: :clapper: :memo: :pencil: :book: :art: :microphone: :headphones: :trumpet: :saxophone: :guitar: :shoe: :sandal: :high_heel: :lipstick: :boot: :shirt: :tshirt: :necktie: :womans_clothes: :dress: :running_shirt_with_sash: :jeans: :kimono: :bikini: :ribbon: :tophat: :crown: :womans_hat: :mans_shoe: :closed_umbrella: :briefcase: :handbag: :pouch: :purse: :eyeglasses: :fishing_pole_and_fish: :coffee: :tea: :sake: :baby_bottle: :beer: :beers: :cocktail: :tropical_drink: :wine_glass: :fork_and_knife: :pizza: :hamburger: :fries: :poultry_leg: :meat_on_bone: :spaghetti: :curry: :fried_shrimp: :bento: :sushi: :fish_cake: :rice_ball: :rice_cracker: :rice: :ramen: :stew: :oden: :dango: :egg: :bread: :doughnut: :custard: :icecream: :ice_cream: :shaved_ice: :birthday: :cake: :cookie: :chocolate_bar: :candy: :lollipop: :honey_pot: :apple: :green_apple: :tangerine: :lemon: :cherries: :grapes: :watermelon: :strawberry: :peach: :melon: :banana: :pear: :pineapple: :sweet_potato: :eggplant: :tomato: :corn:".split(" "),
7:":house: :house_with_garden: :school: :office: :post_office: :hospital: :bank: :convenience_store: :love_hotel: :hotel: :wedding: :church: :department_store: :european_post_office: :city_sunrise: :city_sunset: :japanese_castle: :european_castle: :tent: :factory: :tokyo_tower: :japan: :mount_fuji: :sunrise_over_mountains: :sunrise: :stars: :statue_of_liberty: :bridge_at_night: :carousel_horse: :rainbow: :ferris_wheel: :fountain: :roller_coaster: :ship: :speedboat: :boat: :sailboat: :rowboat: :anchor: :rocket: :airplane: :helicopter: :steam_locomotive: :tram: :mountain_railway: :bike: :aerial_tramway: :suspension_railway: :mountain_cableway: :tractor: :blue_car: :oncoming_automobile: :car: :red_car: :taxi: :oncoming_taxi: :articulated_lorry: :bus: :oncoming_bus: :rotating_light: :police_car: :oncoming_police_car: :fire_engine: :ambulance: :minibus: :truck: :train: :station: :train2: :bullettrain_front: :bullettrain_side: :light_rail: :monorail: :railway_car: :trolleybus: :ticket: :fuelpump: :vertical_traffic_light: :traffic_light: :warning: :construction: :beginner: :atm: :slot_machine: :busstop: :barber: :hotsprings: :checkered_flag: :crossed_flags: :izakaya_lantern: :moyai: :circus_tent: :performing_arts: :round_pushpin: :triangular_flag_on_post: :jp: :kr: :cn: :us: :fr: :es: :it: :ru: :gb: :uk: :de:".split(" "),
8:":one: :two: :three: :four: :five: :six: :seven: :eight: :nine: :keycap_ten: :1234: :zero: :hash: :symbols: :arrow_backward: :arrow_down: :arrow_forward: :arrow_left: :capital_abcd: :abcd: :abc: :arrow_lower_left: :arrow_lower_right: :arrow_right: :arrow_up: :arrow_upper_left: :arrow_upper_right: :arrow_double_down: :arrow_double_up: :arrow_down_small: :arrow_heading_down: :arrow_heading_up: :leftwards_arrow_with_hook: :arrow_right_hook: :left_right_arrow: :arrow_up_down: :arrow_up_small: :arrows_clockwise: :arrows_counterclockwise: :rewind: :fast_forward: :information_source: :ok: :twisted_rightwards_arrows: :repeat: :repeat_one: :new: :top: :up: :cool: :free: :ng: :cinema: :koko: :signal_strength: :u5272: :u5408: :u55b6: :u6307: :u6708: :u6709: :u6e80: :u7121: :u7533: :u7a7a: :u7981: :sa: :restroom: :mens: :womens: :baby_symbol: :no_smoking: :parking: :wheelchair: :metro: :baggage_claim: :accept: :wc: :potable_water: :put_litter_in_its_place: :secret: :congratulations: :m: :passport_control: :left_luggage: :customs: :ideograph_advantage: :cl: :sos: :id: :no_entry_sign: :underage: :no_mobile_phones: :do_not_litter: :non-potable_water: :no_bicycles: :no_pedestrians: :children_crossing: :no_entry: :eight_spoked_asterisk: :eight_pointed_black_star: :heart_decoration: :vs: :vibration_mode: :mobile_phone_off: :chart: :currency_exchange: :aries: :taurus: :gemini: :cancer: :leo: :virgo: :libra: :scorpius: :sagittarius: :capricorn: :aquarius: :pisces: :ophiuchus: :six_pointed_star: :negative_squared_cross_mark: :a: :b: :ab: :o2: :diamond_shape_with_a_dot_inside: :recycle: :end: :on: :soon: :clock1: :clock130: :clock10: :clock1030: :clock11: :clock1130: :clock12: :clock1230: :clock2: :clock230: :clock3: :clock330: :clock4: :clock430: :clock5: :clock530: :clock6: :clock630: :clock7: :clock730: :clock8: :clock830: :clock9: :clock930: :heavy_dollar_sign: :copyright: :registered: :tm: :x: :heavy_exclamation_mark: :bangbang: :interrobang: :o: :heavy_multiplication_x: :heavy_plus_sign: :heavy_minus_sign: :heavy_division_sign: :white_flower: :100: :heavy_check_mark: :ballot_box_with_check: :radio_button: :link: :curly_loop: :wavy_dash: :part_alternation_mark: :trident: :white_check_mark: :black_square_button: :white_square_button: :black_circle: :white_circle: :red_circle: :large_blue_circle: :large_blue_diamond: :large_orange_diamond: :small_blue_diamond: :small_orange_diamond: :small_red_triangle: :small_red_triangle_down: :shipit:".split(" ")};
this.initUI()},initUI:function(){var b=this,d=a("<div/>",{"class":"dialog-header"}),c=a("<div/>",{"class":"dialog-body"}).css({height:"252px"}),f=a("<div/>",{id:"dialog-emoticons-panelLeft"}).css({position:"absolute",left:"0",width:"140px",height:"100%","overflow-x":"hidden","overflow-y":"auto",background:"black"}),g=a("<ul/>",{}).css({"list-style-type":"none",padding:"0 0 160px 0",margin:"0"}),e=a("<div/>",{}).css({position:"absolute",left:"140px",width:"1px",height:"100%","background-color":"#444"}),
h=a("<div/>",{id:"dialog-emoticons-panelRight"}).css({position:"absolute",left:"141px",width:"216px",height:"100%","overflow-x":"hidden","overflow-y":"auto",background:"#808080"}),v=a("<ul/>",{}).css({"list-style-type":"none",margin:"10px auto 0 auto",padding:"0 0 200px 0",width:"184px",overflow:"hidden"}),t=a("<div/>",{id:"dialog-emoticons","class":"dialog"}).css({"z-index":"100",position:"absolute",width:"357px",height:"290px"}),u="";a.each(this.tabs,function(a,d){u+='<li class="emoticons-tab"> <span class="playlist-row-label playlist-row-name">'+
d.name+'</span> <span class="playlist-row-label playlist-row-count">'+(0<=d.index?b.emo[d.index].length:"0")+" items</span> </li>"});injectStyles(".emoticons-tab { position: relative; width: 100%; height: 35px; cursor: pointer; }");injectStyles(".emoticons-tab .playlist-row-label { left: 12px; top: 4px; }");injectStyles(".emoticons-tab .playlist-row-count { top: 20px; }");injectStyles("#dialog-emoticons-panelRight ul li { display: inline-block; margin: 1px; float: left; width:"+this.BLOCK_WIDTH*this.SPRITE_SCALE+
"px; height:"+this.BLOCK_HEIGHT*this.SPRITE_SCALE+"px; overflow: hidden; cursor: pointer; }");injectStyles("#dialog-emoticons-panelRight ul li .emoji { width:"+this.BLOCK_WIDTH*this.SPRITE_SCALE+"px; height:"+this.BLOCK_HEIGHT*this.SPRITE_SCALE+"px; background-size:"+this.SPRITE_WIDTH*this.SPRITE_SCALE+"px "+this.SPRITE_HEIGHT*this.SPRITE_SCALE+"px; }");g.html(u);g.appendTo(f);f.appendTo(c);e.appendTo(c);v.appendTo(h);h.appendTo(c);d.html('<div class="dialog-header"> <p style=" position: absolute; left: 115px; top: 0px; color: lightsteelblue ">CTRL + Click to add continuously</p> <span>Emoticons</span> <div class="dialog-close-button"></div> <div class="dialog-header-line"></div> </div>');
d.appendTo(t);c.appendTo(t);this.dialog=t},getNewBlock:function(b){var d=a("<li/>",{title:""}),c=C.emojify(B.cleanTypedString(b));d.prop("title",b);d.html(c);c=d.children(".emoji-glow").children("span");if(0===c.length)return console.log("Non-existed emoji detected: "+b),null;this.initSpanEmoji(c);return d},initSpanEmoji:function(b){var d,c,f;d=b.clone();a("body").append(d);c=d.css("background-position").split(" ");f=parseInt(c[0].substr(0,c[0].length-2));c=parseInt(c[1].substr(0,c[1].length-2));
b.css("background-position",f*this.SPRITE_SCALE+"px "+c*this.SPRITE_SCALE+"px");d.remove()},initHandlers1:function(){a("#emoji-button").click(a.proxy(this.onShowButtonClick,this))},initHandlers2:function(){if(!this.hasInitHandlers2){var b=this;a("#dialog-emoticons .dialog-close-button").live("click",a.proxy(this.onCloseButtonClick,this));a("#dialog-emoticons").live("mouseover",a.proxy(this.onMouseOverDialog,this));a("#dialog-emoticons").live("mouseout",a.proxy(this.onMouseOutDialog,this));a("body").live("mouseout",
a.proxy(this.onMouseOutDialog,this));a(".emoticons-tab").live("click",function(d){d.handled||(d=a(this).index(),b.updateTab(d));return!1});a("#dialog-emoticons-panelRight ul li").live("mouseenter",function(){event.handled||(a(this).css("background","white"),event.handled=!0);return!1});a("#dialog-emoticons-panelRight ul li").live("mouseleave",function(){event.handled||(a(this).css("background",""),event.handled=!0);return!1});a("#dialog-emoticons-panelRight ul li").live("click",function(d){d.handled||
(b.insertChat(a(this).prop("title")),!b.conti&&b.close(),d.handled=!0);return!1});this.hasInitHandlers2=!0}},initHandlers3:function(){a("#dialog-emoticons-panelLeft").off("scroll",a.proxy(this.onPanelLeftScroll,this)).on("scroll",a.proxy(this.onPanelLeftScroll,this));a("#dialog-emoticons-panelRight").off("scroll",a.proxy(this.onPanelRightScroll,this)).on("scroll",a.proxy(this.onPanelRightScroll,this))},show:function(){a("#dialog-emoticons").remove();this.dialog.appendTo(a("body"));this.updateTab(this.currentTab);
this.repos();this.preventScroll=!0;this.scrollTop.left?a("#dialog-emoticons-panelLeft").scrollTop(this.scrollTop.left):a("#dialog-emoticons-panelLeft").scrollTop(0);this.preventScroll=!1;a("#chat-input-field").focus();this.initHandlers2();this.initHandlers3();this.visible=!0},close:function(){a("#dialog-emoticons").remove();a("#chat-input-field").focus();this.visible=!1},repos:function(){"block"!==a("#button-chat-expand").css("display")?a("#dialog-emoticons").css({top:a("#emoji-button").offset().top-
a("#dialog-emoticons").height()-10,left:a("#emoji-button").offset().left-a("#dialog-emoticons").width()+32}):a("#dialog-emoticons").css({top:a("#emoji-button").offset().top+26,left:a("#emoji-button").offset().left-a("#dialog-emoticons").width()+32})},updateTab:function(b){var d=this;a(".emoticons-tab:lt("+b+")").removeClass("playlist-row-visible");a(".emoticons-tab").eq(b).addClass("playlist-row-visible");a(".emoticons-tab:gt("+b+")").removeClass("playlist-row-visible");if("undefined"===typeof this.rightItems[b]){var c=
"";a.each(this.emo[b],function(a,b){var e=d.getNewBlock(b);c+=e[0].outerHTML});this.rightItems[b]=c}a("#dialog-emoticons-panelRight ul").html(this.rightItems[b]);this.preventScroll=!0;this.scrollTop[b]?a("#dialog-emoticons-panelRight").scrollTop(this.scrollTop[b]):a("#dialog-emoticons-panelRight").scrollTop(0);this.preventScroll=!1;a("#chat-input-field").focus();this.currentTab=b},updateRightPanel:function(b){0<=b&&a("#dialog-emoticons-panelRight ul").html(this.rightItems[b])},addRecentItem:function(b,
d){b=this.replaceCons(b);if(!0!==this.recentItems[d][b]){var c=a("<ul/>",{}),f=this.getNewBlock(b);null!==f&&(c.html(this.rightItems[d]),c.children("li").length+1>this.MAX_RECENT[d]&&(c.children("li:last()").remove(),this.recentItems[d][b]=!1),f.prependTo(c),this.recentItems[d][b]=!0,this.rightItems[d]=c.html(),this.dialog.find(".emoticons-tab").eq(d).children(".playlist-row-count").text(c.children("li").length+" items"),this.currentTab===d&&this.updateRightPanel(d))}},replaceCons:function(b){a.each(this.cons,
function(a,c){if(b===":"+c+":")return b=a});return b},insertChat:function(b){var d=a("#chat-input-field"),c=d.prop("selectionStart"),f=d.prop("selectionEnd"),g=d.val(),e=g.substring(0,c),f=g.substring(f,g.length),h=g=0;0<e.length&&" "!==e[e.length-1]&&(e+=" ",g=1);" "!==f[0]&&(f=" "+f,h=1);d.val(e+b+f);d.prop("selectionStart",c+g+h+b.length);d.prop("selectionEnd",c+g+h+b.length)},setChat:function(b){a("#chat-input-field").val(b).prop("selectionStart",b.length)},switchAutoHide:function(a){this.autoHide=
a},onShowButtonClick:function(){this.show()},onCloseButtonClick:function(){this.close()},onMouseOverDialog:function(){clearTimeout(this.timeout_fadeDialog)},onMouseOutDialog:function(b){if(this.autoHide&&this.visible){var d=a("#dialog-emoticons"),c=d.offset().left,f=d.offset().top,g=d.width(),d=d.height();b.pageX>=c&&b.pageX<=c+g&&b.pageY>=f&&b.pageY<=f+d||(this.timeout_fadeDialog=setTimeout(a.proxy(this.onTimeoutFadeDialog,this),this.TIMEOUT_FADEDiALOG))}},onPanelLeftScroll:function(){this.preventScroll||
(this.scrollTop.left=a("#dialog-emoticons-panelLeft").scrollTop())},onPanelRightScroll:function(){this.preventScroll||(this.scrollTop[this.currentTab]=a("#dialog-emoticons-panelRight").scrollTop())},onTimeoutFadeDialog:function(){clearTimeout(this.timeout_fadeDialog);this.close()},onChatReceived:function(a){var d=a.from,c=API.getUser().username;a=a.message;"undefined"===typeof d&&(d=c);d===c&&(this.historyMessage.length+1>this.MAX_HISTORYChAT&&this.historyMessage.shift(),this.historyMessage.push(a.replace(/&lt;/g,
"<").replace(/&gt;/g,">")));var f=this.cons,g=/:([^ :]+):/;a=a.replace(/</g,"&lt;").replace(/>/g,"&gt;");": "==a.substr(0,2)&&(a=a.substr(2));for(var e in f){var h=e,v=f[e],h=h.replace("<","&lt;").replace(">","&gt;"),h=RegExp("(\\s|^)("+(h+"").replace(/([\\\.\+\*\?\[\^\]\$\(\)\{\}\=\!\<\>\|\:])/g,"\\$1")+")(?=\\s|$)","g");a=a.replace(h,"$1:"+v+":")}for(e=g.exec(a);e;)d===c?this.addRecentItem(e[0],this.TAB_RECENTMe):this.addRecentItem(e[0],this.TAB_RECENTUsERS),a=a.substr(0,e.index)+a.substr(e.index+
e[0].length),e=g.exec(a)},onBodyKeydown:function(b){this.KEYCODE_CONTI===b.which&&(this.conti=!0);this.KEYCODE_ESC===b.which&&a("#chat-input-field").focus()},onBodyKeyup:function(a){this.KEYCODE_CONTI===a.which&&(this.conti=!1)},onChatInputKeydown:function(b){if(this.KEYCODE_ESC===b.which)this.setChat("");else{var d=a("#chat-input-field");this.historyConti?this.KEYCODE_ARROWUp===b.which?(this.historyIndex-=1,-1!==this.historyIndex?(b.preventDefault(),this.setChat(this.historyMessage[this.historyIndex])):
this.historyIndex=0):this.KEYCODE_ARROWDoWN===b.which?(this.historyIndex+=1,this.historyIndex<this.historyMessage.length?(b.preventDefault(),this.setChat(this.historyMessage[this.historyIndex])):this.historyIndex=this.historyMessage.length-1):this.historyConti=!1:this.KEYCODE_ARROWUp===b.which&&""===d.val()&&(this.historyIndex=this.historyMessage.length-1,-1!==this.historyIndex&&(b.preventDefault(),this.setChat(this.historyMessage[this.historyIndex]),this.historyConti=!0))}}}))});
define("app/models/3rd/PlugBot","jquery app/base/Context app/models/PlaybackModel app/views/room/PlaybackView app/models/RoomModel app/views/room/meta/AvatarRolloverView app/models/3rd/EmojiUI".split(" "),function(a,x,B,C,b,d,c){function f(){API.on(API.DJ_ADVANCE,h);API.on(API.WAIT_LIST_UPDATE,v);API.on(API.DJ_UPDATE,v);API.on(API.VOTE_UPDATE,function(a){n()});API.on(API.USER_JOIN,function(a){n()});API.on(API.USER_LEAVE,function(a){n()});API.on(API.CHAT,c.onChatReceived,c);x.on("chat:send",c.onChatReceived,
c)}function g(){a("#plugbot-ui").remove();a("#chat").prepend('<div id="plugbot-ui" class="unselectable"></div>');var b=m?"#3FFF00":"#ED1C24",d=p?"#3FFF00":"#ED1C24",c=q?"#3FFF00":"#ED1C24",f=k?"#3FFF00":"#ED1C24",e=s?"#3FFF00":"#ED1C24";a("#plugbot-ui").append('<p id="plugbot-btn-woot" style="color:'+b+'">auto-woot</p><p id="plugbot-btn-meh" style="color:'+d+'">auto-meh</p><p id="plugbot-btn-queue" style="color:'+c+'">auto-queue</p><p id="plugbot-btn-hidevideo" style="color:'+f+'">hide video</p><p id="plugbot-btn-skipvideo" style="color:#ED1C24">skip video</p><p id="plugbot-btn-userlist" style="color:'+
e+'">userlist</p><p><a href="'+D+'" target="_blank" id="plugbot-btn-openvid" style="color:#FFF">open video link</a></p>')}function e(){a(window).resize(function(){c.repos()});a("body").keydown(a.proxy(c.onBodyKeydown,c)).keyup(a.proxy(c.onBodyKeyup,c));a("#chat-input-field").keydown(a.proxy(c.onChatInputKeydown,c));a("#button-chat-expand").click(function(){setTimeout(function(){c.repos()},100)});a("#button-chat-collapse").click(function(){setTimeout(function(){c.repos()},100)});a("#plugbot-btn-userlist").live("click",
function(){s=!s;a(this).css("color",s?"#3FFF00":"#ED1C24");a("#plugbot-userlist").css("visibility",s?"visible":"hidden");s?(y=0,n()):a("#plugbot-userlist").empty();jaaulde.utils.cookies.set(I,s)});a("#plugbot-btn-woot").live("click",function(){(m=!m)&&(p=!1);a(this).css("color",m?"#3FFF00":"#ED1C24");a("#plugbot-btn-meh").css("color",p?"#3FFF00":"#ED1C24");m&&a("#button-vote-positive").click();jaaulde.utils.cookies.set(J,m)});a("#plugbot-btn-meh").live("click",function(){(p=!p)&&(m=!1);a(this).css("color",
p?"#3FFF00":"#ED1C24");a("#plugbot-btn-woot").css("color",m?"#3FFF00":"#ED1C24");p&&a("#button-vote-negative").click()});a("#plugbot-btn-hidevideo").live("click",function(){k=!k;a(this).css("color",k?"#3FFF00":"#ED1C24");a(this).text(k?"hiding video":"hide video");a("#yt-frame").animate({height:k?"0px":"271px"},{duration:"fast"});a("#playback .frame-background").animate({opacity:k?"0":"0.91"},{duration:"medium"});jaaulde.utils.cookies.set(K,k)});a("#plugbot-btn-skipvideo").live("click",function(){l=
!l;a(this).css("color",l?"#3FFF00":"#ED1C24");a(this).text(l?"skipping video":"skip video");var b=API.getVolume();l?(E=b,API.setVolume(0)):API.setVolume(E);l?(w||k||a("#plugbot-btn-hidevideo").click(),w=!0):(w&&k&&a("#plugbot-btn-hidevideo").click(),w=!1)});a("#plugbot-btn-queue").live("click",function(){q=!q;a(this).css("color",q?"#3FFF00":"#ED1C24");q&&!t()&&u();jaaulde.utils.cookies.set(L,q)});a(".plugbot-userlist-user").live("click",function(){var c=a(this).position(),Q=a(this).text(),f=null;
a.each(b.get("users"),function(a,b){if(b.get("username")===Q)return f=b,!1});d.showChat(f,{x:c.left+300,y:c.top})});R()}function h(b){k&&!l&&(a("#yt-frame").css("height","0px"),a("#playback .frame-background").css("opacity",".0"));l&&(a("#plugbot-btn-skipvideo").css("color","#ED1C24").text("skip video"),w&&k&&a("#plugbot-btn-hidevideo").click(),API.setVolume(E),C.onRefreshClick(),w=l=!1);m?a("#button-vote-positive").click():p&&a("#button-vote-negative").click();n();M(!1)}function v(){q&&!t()&&u();
y=0;n()}function t(){return-1!==API.getBoothPosition()||-1!==API.getWaitListPosition()}function u(){"block"===a("#button-dj-play").css("display")?a("#button-dj-play").click():API.getWaitList().length<S&&API.djJoin()}function n(){if(s&&F){var b=new Date,c=b.getTime(),b=null;clearTimeout(N);if(c-y>=O){y=c;b=a("#plugbot-userlist");c=API.getUsers();b.html(" ").append('<h1 style="text-indent:12px;color:#42A5DC;font-size:14px;font-variant:small-caps;">Users: '+c.length+"</h1>").append('<p style="padding-left:12px;text-indent:0px !important;font-style:italic;color:#42A5DC;font-size:11px;">Click a username to<br />open user-box!</p><br />');
if(""!==a("#button-dj-waitlist-view").prop("title")&&"block"===a("#button-dj-waitlist-leave").css("display")&&-1==a.inArray(API.getDJs(),API.getUser())){var d=a("#button-dj-waitlist-view").prop("title").split("(")[1],d=d.substring(0,d.indexOf(")"));b.append('<h1 id="plugbot-queuespot"><span style="font-variant:small-caps">Waitlist:</span> '+d+"</h1><br />")}a.each(c,function(a,b){var c=b.username,d=+b.permission,H=API.getDJs()[0],f=!1;"undefined"!==H&&(f=H.username==c);var e;switch(d){case 0:e="normal";
break;case 1:e="featured";break;case 2:e="bouncer";break;case 3:e="manager";break;case 4:case 5:e="host";break;case 9:case 10:e="admin"}f?"normal"===e?A("void","#42A5DC",c):A(e+"_current.png","#42A5DC",c):"normal"===e?A("void",G(b.vote),c):A(e+T(b.vote),G(b.vote),c)})}else N=setTimeout(function(){n()},O)}}function G(a){if(!a)return"#fff";switch(a){case -1:return"#c8303d";case 0:return"#fff";case 1:return"#c2e320"}}function T(a){if(!a)return"_undecided.png";switch(a){case -1:return"_meh.png";case 0:return"_undecided.png";
case 1:return"_woot.png"}}function A(b,c,d){var e=API.getDJs()[0],f=!1;"undefined"!==e&&(f=e.username==d);"void"!==b&&(e="http://www.theedmbasement.com/basebot/userlist/"+b,a("#plugbot-userlist").append('<img src="'+e+'" align="left" style="margin-left:6px;margin-top:2px" />'));a("#plugbot-userlist").append('<p class="plugbot-userlist-user" style="cursor:pointer;'+("void"===b?"":"text-indent:6px !important;")+"color:"+c+";"+(f?"font-size:15px;font-weight:bold;":"")+'" >'+d+"</p>")}function P(){var b=
new Date;b.setFullYear(b.getFullYear()+1);jaaulde.utils.cookies.setOptions({expiresAt:b});b=jaaulde.utils.cookies.get(J);m=null!=b?b:!0;b=jaaulde.utils.cookies.get(L);q=null!=b?b:!1;b=jaaulde.utils.cookies.get(K);k=null!=b?b:!1;b=jaaulde.utils.cookies.get(I);s=null!=b?b:!0;m?a("#button-vote-positive").click():p&&a("#button-vote-negative").click();q&&!t()&&u();k&&(a("#yt-frame").animate({height:k?"0px":"271px"},{duration:"fast"}),a("#playback .frame-background").animate({opacity:k?"0":"0.91"},{duration:"medium"}));
n();U(V);injectStyles(".unselectable { -moz-user-select: -moz-none; -khtml-user-select: none; -webkit-user-select: none; -o-user-select: none; user-select: none; }");M(!0);W();f();g();e();var b=a(".chat-input"),d=a("#chat-input-field");a("#dialog-box");var h=a("<span/>",{"class":"emoji emoji-1f603"}).css({margin:"3px 0 0 3px"}),l=a("<div/>",{id:"emoji-button",title:"Insert Emoticons"}).css({position:"absolute",width:"22",height:"24",right:"0",cursor:"pointer"});a("#emoji-button").remove();a("#dialog-emoticons").remove();
d.css("width","267px");h.appendTo(l);l.appendTo(b);c.initHandlers1()}function V(){y=0;setTimeout(function(){h(null)},1E3)}function U(a){var b="",c,d;d=function(){0!==API.getUsers().length&&(a(),clearInterval(c))};setInterval(function(){window.location.href!=b&&(""!==b&&(c=setInterval(d,100)),b=window.location.href)},100)}function M(a){var b=B.get("media");if("undefined"!==typeof b){var c=b.get("format"),b=b.get("cid");"1"===c?D="http://www.youtube.com/watch?v="+b:"2"===c&&(D="http://www.soundcloud.com/");
a||g()}}function W(){window.alert=function(a){console.log("ALERT: "+a)}}function R(){function a(c){var d=!0;c=c||window.event;(d="focus"==c.type||"focusin"==c.type?!0:"blur"==c.type||"focusout"==c.type?!1:!this[b])?(F=!0,n()):F=!1}var b="hidden";b in document?document.addEventListener("visibilitychange",a):(b="mozHidden")in document?document.addEventListener("mozvisibilitychange",a):(b="webkitHidden")in document?document.addEventListener("webkitvisibilitychange",a):(b="msHidden")in document?document.addEventListener("msvisibilitychange",
a):"onfocusin"in document?document.onfocusin=document.onfocusout=a:window.onfocus=window.onblur=a}var m,p=!1,q,k,s,N,y=0,O=3E3,l=!1,E=50,w=!1,D="",F=!0,J="autowoot",L="autoqueue",K="hidevideo",I="userlist",S=50;a("#plugbot-userlist").remove();a("#plugbot-css").remove();a("#plugbot-js").remove();var X=document.getElementsByTagName("head")[0],z=document.createElement("script");z.type="text/javascript";z.src="http://cookies.googlecode.com/svn/trunk/jaaulde.cookies.js";z.onreadystatechange=function(){"complete"==
this.readyState&&P()};z.onload=P;X.appendChild(z);a("body").prepend('<style type="text/css" id="plugbot-css">#plugbot-ui { position: absolute; margin-left: 349px; }#plugbot-ui p { background-color: #0b0b0b; height: 32px; padding-top: 8px; padding-left: 8px; padding-right: 6px; cursor: pointer; font-variant: small-caps; width: 84px; font-size: 15px; margin: 0; }#plugbot-ui h2 { background-color: #0b0b0b; height: 112px; width: 156px; margin: 0; color: #fff; font-size: 13px; font-variant: small-caps; padding: 8px 0 0 12px; border-top: 1px dotted #292929; }#plugbot-userlist { border: 6px solid rgba(10, 10, 10, 0.8); border-left: 0 !important; background-color: #000000; padding: 8px 0px 20px 0px; width: 12%; }#plugbot-userlist p { margin: 0; padding-top: 4px; text-indent: 24px; font-size: 10px; }#plugbot-userlist p:first-child { padding-top: 0px !important; }#plugbot-queuespot { color: #42A5DC; text-align: left; font-size: 15px; margin-left: 8px }');
a("body").append('<div id="plugbot-userlist"></div>')});function injectStyles(a){$("head").append('<style type="text/css">'+a+"</style>")};
