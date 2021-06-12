@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/SettingsIcons.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/UsrBgs.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BlurpleRecolor/BlurpleRecolor.css);

:root {
	--transparencycolor:			0,0,0;
	--transparencyalpha:			0.0;
	--messagetransparency:			0.5;
	--usechatbubbles: 				calc(var(--messagetransparency) / (var(--messagetransparency) + 0.00000000000000000000001));
	--guildchanneltransparency:		0.0;
	--chatinputtransparency:		0.0;
	--memberlisttransparency:		0.0;
	
	--font:							Whitney, Helvetica Neue, Helvetica, Arial, sans-serif;
	--textshadow:					transparent;
	
	--accentcolor:					190,78,180;
	--accentcolor2:					var(--accentcolor);
	--linkcolor:					var(--accentcolor);
	
	--successcolor: 				59,165,92;
	--warningcolor: 				250,166,26;
	--dangercolor: 					237,66,69;
	
	--textbrightest: 				255,255,255;
	--textbrighter: 				222,222,222;
	--textbright: 					200,200,200;
	--textdark: 					160,160,160;
	--textdarker: 					125,125,125;
	--textdarkest: 					90,90,90;
	
	--background:					url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BasicBackground/_res/background.jpg);
	--backgroundposition:			center;
	--backgroundsize:				cover;
	--backgroundblur:				unset;
	
	--popout:						var(--background);
	--popoutposition:				var(--backgroundposition);
	--popoutsize:					var(--backgroundsize);
	--popoutblur:					var(--backgroundblur);
	
	--backdrop:						rgba(0,0,0,0.85);
	--backdropposition:				var(--backgroundposition);
	--backdropsize:					var(--backgroundsize);
	--backdropblur:					var(--backgroundblur);
	
	--bdfdb-green:					rgb(var(--successcolor));
	--bdfdb-yellow:					rgb(var(--warningcolor));
	--bdfdb-red:					rgb(var(--dangercolor));
}

.theme-light, .theme-dark {
	--text-positive: rgb(var(--successcolor));
	--text-warning: rgb(var(--warningcolor));
	--text-danger: rgb(var(--dangercolor));
	--info-positive-background: rgba(var(--successcolor),.1);
	--info-positive-foreground: rgb(var(--successcolor));
	--info-positive-text: #fff;
	--info-warning-background: rgba(var(--warningcolor),.1);
	--info-warning-foreground: rgb(var(--warningcolor));
	--info-warning-text: #fff;
	--info-danger-background: rgba(var(--dangercolor),.1);
	--info-danger-foreground: rgb(var(--dangercolor));
	--info-danger-text: #fff;
	--status-positive-background: rgb(var(--successcolor));
	--status-positive-text: #fff;
	--status-warning-background: rgb(var(--warningcolor));
	--status-warning-text: #fff;
	--status-danger-background: rgb(var(--dangercolor));
	--status-danger-text: #fff;
	--header-primary: rgb(var(--textbrightest));
	--header-secondary: rgb(var(--textbright));
	--text-normal: rgb(var(--textbrighter));
	--text-muted: rgb(var(--textdarker));
	--channels-default: rgb(var(--textdark));
	--interactive-normal: rgb(var(--textbright));
	--interactive-hover: rgb(var(--textbrighter));
	--interactive-active: rgb(var(--textbrightest));
	--interactive-muted: rgb(var(--textdarkest));
	--logo-primary: rgb(var(--textbrightest));
	--background-accent: rgba(var(--transparencycolor), .1);
	--background-primary: rgba(var(--transparencycolor), .2);
	--background-secondary: rgba(var(--transparencycolor), .3);
	--background-secondary-alt: rgba(var(--transparencycolor), .35);
	--background-tertiary: rgba(var(--transparencycolor), .4);
	--background-floating: rgba(var(--transparencycolor), .5);
	--background-modifier-accent: rgba(var(--textbrightest),.1);
	--elevation-low: 0 1px 5px 0 rgba(var(--transparencycolor), .3);
	--elevation-high: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	--font-primary: var(--font) !important;
	--font-display: var(--font) !important;
}


/* ~~~~		0.		TABLE OF CONTENTS				~~~~ */
/*
	1.	TRANSPARENCY
	2.	BACKGROUND
	3.	TITLEBAR
	4.	GUILDLIST
	5.	CHANNELLIST
		1.	GUILDHEADER
		2.	CHANNELS
		3.	DMCHANNELS
		4.	ACCOUNT/VOICE/GOLIVE
	6.	CHAT
		1.	CHANNELHEADER
		2.	MESSAGES
			1.	MESSAGE
			2.	EMBEDS
			3.	NITROGIFT
			4.	INVITE
		3.	TEXTAREA
		4.	AUTOCOMPLETEMENU
		5.	MEMBERLIST
		6.	SEARCHPAGE
		7.	CALL
		8.	UNAVAILABLESCREEN
	7.	PEOPLES
	8.	STORE/NITRO
	9.	LIBRARY
	10.	DISCOVERY
	11.	USERSETTINGS
	12.	GUILDSETTINGS
	13.	MODALS
		1.	USERMODAL
		2.	GUILDADD/CREATION
		3.	REGIONSELECTMODAL
		4.	UPLOADMODAL
		5.	KEYBOARDSHORTCUTSMODAL
		6.	QUICKSWITCHER
		7.	INVITEMODAL/GROUPCREATE
		8.	LOGINSCREEN
		9.	TERMACCEPTMODAL
		10.	DOWNLOADAPPMODAL
		11.	GUILDBOOSTMODAL
		12.	REACTIONSMODAL
		13.	GUILDTEMPLATEMODAL
		14.	GUILDWELCOMEMODAL
		15.	GUILDRULESMODAL
		16.	GUILDFEEDBACKMODAL
		17.	SCREENSHAREMODAL
		18.	PHONEVERIFICATIONMODAL
		19.	NOTIFICATIONSMODAL
		20.	DISCOVERYENTRYMODAL
	14.	POPOUTS
		1.	CONTEXTMENU
		2.	USERPOPOUT
		3.	EMOJIPICKER
		4.	PINS/MENTIONS
		5.	SEARCHPOPOUT
		6.	COLORPICKER
		7.	ADDROLE
		8.	EVERYONEMENTION
		9.	CHANNELFOLLOW
		10.	CHANNELFOLLOWINFO
		11.	EMOJIINFO
		12.	STREAMPREVIEW
		13.	STREAMINFO
		14.	PUBLICGUILDANNOUNCEMENT
		15.	RTCSTATUSPOPOUT
		16.	PHONE-/EMAILVALIDATION
		17.	QUICKSELECTPOPOUT
		18.	WARNINGPOPOUT
	15.	GENERAL
		1.	TEXT
		2.	BUTTONS
		3.	INPUTS
		4.	SEARCHBARS
		5.	TAGS
		6.	ICONS
		7.	SCROLLBARS
		8.	NOTIFICATIONBAR
		9.	TOOLTIPS
	16.	BDSUPPORT
	17.	POWERCORDSUPPORT
	18.	PLUGINSUPPORT
		1.	BDFDB
		2.	DATEVIEWER
		3.	MEMBERCOUNT
		4.	LINENUMBERS
		5.	PERMISSIONVIEWER
		6.	DIRECTDOWNLOAD
		7.	BETTERFORMATINGREDUX
		8.	CHANNELHISTORY
		9.	CHANNELTABS
		10.	TYPINGINDICATOR
		11.	BADGESEVERYWHERE
	19.	UPDATENOTICE
	20.	WATERMARK
*/


/* ~~~~		1.		TRANSPARENCY					~~~~ */

body,														/* body														*/
#app-mount .app-1q1i1E,										/* app					container							*/
#app-mount .app-2rEoOp,										/* app					inner								*/
#app-mount .loading-Ags1CY,									/* app					i18n loading						*/
#app-mount .wrapper-1prNyd,									/* app					errorscreen							*/
#app-mount .bg-h5JY_x,										/* app					background							*/
#app-mount .layer-3QrUeG,									/* layer				container							*/
#app-mount .container-3w7J-x,								/* channels				inner								*/
#app-mount .privateChannels-1nO12o,							/* dmchannels												*/
#app-mount .panels-j1Uci_ > *,								/* account/voice		inner								*/
#app-mount .chat-3bRxxu,									/* chat					container							*/
#app-mount .wrapper-3vR61M,									/* chat					messages loading					*/
#app-mount .noChannel-Z1DQK7,								/* nochannel												*/
#app-mount .members-1998pB,									/* members													*/
#app-mount .members-1998pB > div,							/* members				content								*/
#app-mount .content-MLh4nU,									/* unavailable												*/
#app-mount .container-1D34oG,								/* peoples													*/
#app-mount .container-lRFx4q,								/* peoples				activity list						*/
#app-mount .applicationStore-1pNvnv,						/* nitro													*/
#app-mount .pageWrapper-1PgVDX,								/* guilddiscovery											*/
#app-mount .scrollerBase-289Jih,							/* scroller													*/
#app-mount .scroller-2FKFPG,								/* scroller old												*/
#app-mount .standardSidebarView-3F1I7i,						/* settings													*/
#app-mount .contentRegion-3nDuYy {							/* settings				content								*/
	background: transparent;
}

#app-mount .scroller-2ZPeAD {								/* peoples				activity scroller					*/
	border: none;
}

#app-mount .sidebarRegion-VFTUkN {							/* settings				sidebar								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .sidebar-_0OpfR {								/* sidebarlist			sidebar								*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount {												/* app-mount												*/
	background-color: rgba(var(--transparencycolor), var(--transparencyalpha));
}
#app-mount .wrapper-3NnKdC {								/* guilds				container							*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 2));
}
#app-mount .sidebar-2K8pFh {								/* channels				container							*/
	background-color: rgba(var(--transparencycolor), var(--guildchanneltransparency));
}
#app-mount .panels-j1Uci_ {									/* account/voice		container							*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) / 1.5));
}
#app-mount .container-1r6BKw.themed-ANHk51 {				/* channelheader		container							*/
	background-color: rgba(var(--transparencycolor), var(--guildchanneltransparency));
}
#app-mount .membersWrap-2h-GB4 {							/* members				container							*/
	background-color: rgba(var(--transparencycolor), var(--memberlisttransparency));
}
#app-mount .tabBar-fg4VK9 {									/* members				tabbar								*/
	background-color: rgba(var(--transparencycolor), var(--memberlisttransparency));
}
#app-mount .nowPlayingColumn-2sl4cE {						/* peoples				now playing							*/
	background-color: rgba(var(--transparencycolor), var(--memberlisttransparency));
}

#app-mount .image-3zK3Wt {									/* app					errorscreen image					*/
	background-image: url(https://discord.com/assets/e9baf4b505eb54129f832556ea16538e.svg);
	opacity: 0.6;
}


/* ~~~~		2.		BACKGROUND						~~~~ */

body::before {
	content: "";
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	filter: blur(var(--backgroundblur));
}
.container-16j22k::before,
.layer-3QrUeG ~ .layer-3QrUeG::before,
.root-3R2ngo::before {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
	pointer-events: none;
	z-index: -1;
}
.container-16j22k::after,
.layer-3QrUeG ~ .layer-3QrUeG::after,
.root-3R2ngo::after {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background-color: rgba(var(--transparencycolor), var(--transparencyalpha));
	pointer-events: none;
	z-index: -1;
}
#ace_settingsmenu_container,
.uploadArea-3QgLtW,
.backdrop-29yll0,
.backdrop-1wrmKB {
	background: var(--backdrop) var(--backdropposition)/var(--backdropsize) !important;
	filter: blur(var(--backdropblur));
	opacity: 1;
	animation: none;
}
.withLayer-RoELSG {
	z-index: -1;
}


/* ~~~~		3.		TITLEBAR						~~~~ */

.titleBar-AC4pGV {
	z-index: 5001;
}
.titleBar-AC4pGV::after {
	content: "";
	pointer-events: none;
	position: absolute;
	z-index: -1;
	top: 0;
	left: 0;
	width: 100%;
	background-color: rgba(var(--transparencycolor), calc(0.1 + var(--guildchanneltransparency) * 2));
}
.titleBar-AC4pGV:not(.typeMacOS-3EmCyP)::after {
	height: 22px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP::after {
	height: 28px;
	width: calc(100% - 4px);
	margin: 2px;
	border-radius: 5px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP,
.titleBar-AC4pGV.typeMacOS-3EmCyP .macButtons-2MuSAC {
	width: 72px;
}
.titleBar-AC4pGV.typeMacOS-3EmCyP.typeMacOSWithFrame-3R_i5S .macButtons-2MuSAC {
	margin-top: 0;
	margin-right: 0;
}
.platform-osx .wrapper-3NnKdC {
	margin-top: 0;
	padding-top: 32px;
}
.platform-osx .standardSidebarView-3F1I7i::before {
	left: 72px;
}
.winButtonMinMax-PBQ2gm:hover {
	background-color: rgba(var(--transparencycolor), .2);
}


/* ~~~~		4.		GUILDLIST						~~~~ */

.childWrapper-anI2G9,										/* homebutton/acronym	innerwrap							*/
#bd-pub-button {											/* publicbutton			innerwrap							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--text-normal);
	font-weight: 500;
}
.wrapper-1BJsBx:hover .childWrapper-anI2G9,
.wrapper-1BJsBx.selected-bZ3Lue .childWrapper-anI2G9,
#bd-pub-button:hover {
	text-shadow: 1px 1px var(--textshadow);
}
.noIcon-1a_FrS {											/* acronym				minicontainer						*/
	background-color: rgba(var(--transparencycolor), .3);
}

.circleIconButton-1QV--U {									/* guildadd/discovery	innerwrap							*/
	background-color: rgba(var(--transparencycolor), .3);
}

.guildIconUnavailable-3IYARS,								/* guilderror			miniicon							*/
.guildsError-g6NwOI {										/* guilderror			innerwrap							*/
	background-color: rgba(var(--dangercolor)),.3);
}

.dragInner-Oq_toX {											/* dragplaceholder											*/
	background-color: rgba(var(--transparencycolor), .3);
}

.wrapper-3Njo_c {											/* folder				outerwrap							*/
	margin-bottom: 8px;
}
.folder-1hbNCn {											/* folder				iconwrap							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.folder-1hbNCn.hover-qTxTR_ {
	background-color: rgba(var(--transparencycolor), .4);
}
.expandedFolderBackground-1cujaW {							/* folder				background							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-radius: 15px 15px 24px 24px;
	top: 0;
	bottom: 0;
	margin-bottom: 8px;
	transition: border-radius 3s ease, background-color 1s ease;
}
.expandedFolderBackground-1cujaW.hover-qTxTR_ {
	background-color: rgba(var(--transparencycolor), .4);
}

.wrapper-3NnKdC .wrapper-3Njo_c [role="group"] {			/* folder				guildwrap							*/
	margin-bottom: -8px;
}
.wrapper-3NnKdC .wrapper-3Njo_c [role="group"] .listItem-GuPuDH:last-child {
	margin-bottom: 0;
}

.bar-30k2ka {												/* guild/channelbar		inner								*/
	box-shadow: 0 2px 6px rgba(var(--transparencycolor), .24);
}
.bar-30k2ka:not(.mention-1f5kbO) {
	background-color: transparent;
	overflow: hidden;
}
.bar-30k2ka:not(.mention-1f5kbO)::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
	pointer-events: none;
	z-index: -1;
}
.bar-30k2ka:not(.mention-1f5kbO)::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	pointer-events: none;
	z-index: -1;
}
.sidebar-2K8pFh .bar-30k2ka:not(.mention-1f5kbO)::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--guildchanneltransparency) * 0.85 + 0.1));
}
.wrapper-3NnKdC .bar-30k2ka:not(.mention-1f5kbO)::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--guildchanneltransparency) * 1.9 + 0.1));
}


/* ~~~~		5.		CHANNELLIST						~~~~ */

#app-mount .sidebar-2K8pFh {								/* channels				container							*/
	border-radius: 0;
}

/* ----		5.1.	GUILDHEADER						---- */

.container-1taM1r .animatedContainer-1NSq4T {				/* banner				wrap								*/
	background: none;
	box-shadow: none;
}
.bannerImage-1jOskm {										/* banner				image								*/
	-webkit-mask: linear-gradient(rgba(0,0,0,0.9) 70%, rgba(0,0,0,0) 100%);
}
.bannerImage-1jOskm::before {
	display: none;
}

.header-2V-4Sw,												/* header				inner								*/
.searchBar-6Kv8R2 {											/* header				searchbar							*/
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
}
.searchBar-6Kv8R2 .searchBarComponent-32dTOx {				/* header				searchbarinner						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.clickable-25tGDB:not(.hasBanner-2SrLR3) .header-2V-4Sw:hover,
.selected-31Nl7x:not(.hasBanner-2SrLR3) .header-2V-4Sw {
	background-color: rgba(var(--transparencycolor), .2);
}

.channelNotice-1-XFjC {										/* notice				container							*/
	box-shadow: inset 0 -1px 0 rgba(var(--transparencycolor), .3);
}
.channelNotice-1-XFjC.invite-OjTXrW,
.channelNotice-1-XFjC.guildMFAWarning-3GEzs8,
.channelNotice-1-XFjC.maxMembersCount-3E4zND,
.channelNotice-3DDmsB,
#app-mount .channelNotice-3hkOiI {
	background: transparent;
}
.channelNotice-1-XFjC.invite-OjTXrW::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/bf625d222187f542b9d7179109422e2c.svg) center 20px no-repeat;
}
.channelNotice-1-XFjC.guildMFAWarning-3GEzs8::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/916a384814e3bbd2a84e2a1b352a17c3.svg) center 20px no-repeat;
}
.channelNotice-1-XFjC.quickswitcher-35bYg4::before {
	opacity: 0.6;
}
.channelNotice-1-XFjC.maxMembersCount-3E4zND::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/01f60394adffda20dc7270a1e3c727df.svg) center 16px no-repeat;
}
.channelNotice-3DDmsB::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/1858873f28bdc62dfb3a1f4b67d459bf.svg) center top 20px/153px no-repeat;
}
#app-mount .channelNotice-3hkOiI::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/7065587bd42fd829925bf6aa4b36f5e2.svg) center top 22px/220px no-repeat;
}

/* ----		5.2.	CHANNELS						---- */

.wrapper-2jXpOf:hover .content-1x5b-n {						/* channel				content								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.modeSelected-346R90 .content-1x5b-n,
.modeSelected-346R90:hover .content-1x5b-n {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.modeSelected-346R90 .content-1x5b-n svg,
.modeSelected-346R90:hover .content-1x5b-n svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.icon-1DeIlz {												/* channel				icon								*/
	color: var(--channels-default);
}
.modeMuted-onO3r- .icon-1DeIlz {
	color: var(--interactive-muted);
}
.modeMuted-onO3r-:hover .icon-1DeIlz,
.wrapper-2jXpOf:hover .icon-1DeIlz {
	color: var(--interactive-hover);
}
.modeConnected-3IsKId .icon-1DeIlz,
.modeConnected-3IsKId:hover .icon-1DeIlz,
.modeSelected-346R90 .icon-1DeIlz,
.modeSelected-346R90:hover .icon-1DeIlz,
.modeUnread-1qO3K1 .icon-1DeIlz,
.modeUnread-1qO3K1:hover .icon-1DeIlz,
.notInteractive-1X92pj.modeConnected-3IsKId .icon-1DeIlz,
.notInteractive-1X92pj.modeSelected-346R90 .icon-1DeIlz {
	color: var(--interactive-active);
}
.modeConnected-3IsKId .subtitle-3V1p2E,						/* channel				subtitle							*/
.modeConnected-3IsKId:hover .subtitle-3V1p2E,
.modeSelected-346R90 .subtitle-3V1p2E,
.modeSelected-346R90:hover .subtitle-3V1p2E,
.modeUnread-1qO3K1 .subtitle-3V1p2E,
.modeUnread-1qO3K1:hover .subtitle-3V1p2E,
.notInteractive-1X92pj.modeConnected-3IsKId .subtitle-3V1p2E,
.notInteractive-1X92pj.modeSelected-346R90 .subtitle-3V1p2E {
	color: var(--interactive-normal);
}

.wrapper-2tAnRe {											/* voicechat			limit								*/
	background-color: rgba(var(--transparencycolor), .15);
}
.wrapper-2tAnRe .users-3kndPl {
	background-color: transparent;
}
.wrapper-2tAnRe .total-i6us2n {
	background-color: rgba(var(--transparencycolor), .3);
}
.wrapper-2tAnRe .total-i6us2n::after {
	border-right-color: rgba(var(--transparencycolor), .3);
}

.listDefault-3ir5aS .clickable-1lCRLF:hover .content-1Wq3SX {
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		5.3.	DMCHANNELS						---- */

.channel-2QD9_O:hover .layout-2DM8Md {						/* dmchannel/page		inner							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.selected-aXhQR6.channel-2QD9_O .layout-2DM8Md {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.selected-aXhQR6.channel-2QD9_O .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.empty-388osJ {												/* loadingplaceholders										*/
	fill: rgba(var(--transparencycolor), .4);
}

/* ----		5.4.	ACCOUNT/VOICE/GOLIVE			---- */

.panels-j1Uci_ > * {										/* account/voice		inner								*/
	border: none;
}
.panels-j1Uci_ > * + * {
	border-top: 1px solid rgba(var(--transparencycolor), .2);
}

.button-14-BFJ.enabled-2cQ-u7 {								/* account/voice		panel button						*/
	opacity: 0.7;
}
.button-14-BFJ.enabled-2cQ-u7:hover {
	opacity: 1;
	background-color: rgb(var(--accentcolor));
}
.button-14-BFJ.enabled-2cQ-u7:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.button-1YfofB.buttonColor-7qQbGO {
	background-color: rgba(var(--transparencycolor), .2);
}
.button-1YfofB.buttonColor-7qQbGO:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp,
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp:hover {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp svg,
.button-1YfofB.buttonColor-7qQbGO.buttonActive-3FrkXp:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}


/* ~~~~		6.		CHAT							~~~~ */

/* ----		6.1.	CHANNELHEADER					---- */

.container-1r6BKw.themed-ANHk51 {							/* header				themedcontainer						*/
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
}

.input-2A_zIr:focus {										/* header				dmchannelinput						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.input-2A_zIr:focus,
.outer-o9SjPm:hover .input-2A_zIr {
	box-shadow: inset 0 0 0 1px rgba(var(--transparencycolor), .2);
}
.children-19S4PO::after {									/* header				topicgradient						*/
	display: none;
}

.akaBadge-1M-1Gw {											/* header				aka									*/
	background-color: rgba(var(--transparencycolor), .3);
}

.badge-2qGa_k::after {										/* header				iconbadge red dot					*/
	border: none;
}

.searchBar-3dMhjb {											/* header				searchbar							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .public-DraftEditorPlaceholder-root {
	color: rgb(var(--textdarker));
}
#app-mount .public-DraftEditorPlaceholder-hasFocus {
	color: var(--header-secondary);
}
#app-mount .searchFilter-2ESiM3,
#app-mount .searchAnswer-3Dz2-q {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		6.2.	MESSAGES						---- */

.emptyChannelIcon-cc932w {									/* welcomemessage		empty channelicon					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.card-1yV8cG {												/* welcomemessage		first steps card					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.card-1yV8cG:hover {
	background-color: rgba(var(--transparencycolor), .5);
}

.button-18p_f6:hover {										/* welcomemessage		edit channel						*/
	background-color: rgb(var(--accentcolor));
	color: var(--interactive-active);
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .role-1P70N6 {									/* welcomemessage		role								*/
	background: transparent;
	border-color: rgba(var(--textbrighter), .6);
	border-radius: 5px;
	height: 22px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-1P70N6[style*="border-color: rgba(185, 187, 190, .6)"] {
	border-color: rgba(var(--textbrighter), .6) !important;
}
#app-mount .role-1P70N6 .roleColor-fHISxl {					/* welcomemessage		rolecircle							*/
	position: absolute;
	background-color: var(--text-normal);
	border-radius: 3px;
	opacity: 0.5;
	height: 100%;
	width: 100%;
	margin: 0;
	left: 0;
	top: 0;
	z-index: -1;
}
#app-mount .role-1P70N6:hover .roleColor-fHISxl {
	opacity: 0.8;
}
#app-mount .role-1P70N6 .roleColor-fHISxl[style*="background-color: rgb(185, 187, 190)"] {
	background-color: var(--text-normal) !important;
}

.divider-JfaTT5.hasContent-1cNJDh {							/* divider				hascontent							*/
	border-color: transparent;
}
.content-1o0f9g {											/* divider				content								*/
	background-color: rgba(var(--transparencycolor), .2);
	width: 100%;
	text-align: center;
}

.hasMore-3POVhk:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.jumpToPresentBar-G1R9s6 {									/* bar					jumptopresent						*/
	background-color: transparent;
	overflow: hidden;
	opacity: 1;
}
.jumpToPresentBar-G1R9s6::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
	pointer-events: none;
	z-index: -1;
}
.jumpToPresentBar-G1R9s6::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	pointer-events: none;
	z-index: -1;
}

/* ====		6.2.1.	MESSAGE							==== */

#app-mount .message-2qRu38 {								/* message				confirm modal						*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
}
.message-2qnXI6,											/* message				container							*/
.messagesWrapper-1sRNjr .wrapper-2a6GCs,					/* message				upload placeholder					*/
.wrapper-1F5TKx,											/* message				loading 							*/
.message-2DieIs,											/* message				mention popout						*/
.message-2g38UB,											/* message				inbox popout						*/
.message-2qRu38 .wrapper-2a6GCs,							/* message				settings preview					*/
.messageGroupCozy-2iY6cT,									/* message				pin popout							*/
.message-1Ng5AR .wrapper-2a6GCs {							/* message				searchpage							*/
	background-color: rgba(var(--transparencycolor), var(--messagetransparency)) !important;
	contain: unset;
}
.message-1Ng5AR .wrapper-2a6GCs {							/* message				searchpage							*/
	background-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 0.8)) !important;
}
.message-2qnXI6.selected-2P5D_Z,
.mouse-mode .message-2qnXI6:hover,
.mouse-mode.full-motion .message-2qnXI6:hover,
.mouse-mode .wrapper-1F5TKx:hover,
.mouse-mode.full-motion .wrapper-1F5TKx:hover {
	background-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 1.2 * var(--usechatbubbles) + 0.3 * (1 - var(--usechatbubbles)))) !important;
}
.backgroundFlash-24qWLN .message-2qnXI6 {					/* message				jump flash							*/
	position: relative;
}
.backgroundFlash-24qWLN .message-2qnXI6::before {
	content: "";
	position: absolute;
	background: var(--message-background-flash, transparent);
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	z-index: 1;
	pointer-events: none;
}
.backgroundFlash-24qWLN .cozyMessage-3V1Y8y::before {
	left: calc(-80px * var(--usechatbubbles));
}
.message-2qnXI6.ephemeral-1PsL1r,							/* message				localbot							*/
.message-2qnXI6.replying-1x3H0T {							/* message				replying							*/
	background-image: linear-gradient(rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))), rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))));
}
.message-2qnXI6.mentioned-xhSam7 {							/* message				mentioned							*/
	background-image: linear-gradient(rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))), rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))));
}
.message-2qnXI6.ephemeral-1PsL1r::before,
.message-2qnXI6.replying-1x3H0T::before,
.message-2qnXI6.mentioned-xhSam7::before {
	background-color: rgb(var(--accentcolor));
}
.message-2qnXI6.mentioned-xhSam7 .contents-2mQqc9 .messageContent-2qWWxC {
	border-radius: 3px;
	background-color: rgba(var(--accentcolor), calc(0.3 * var(--usechatbubbles)));
}
#app-mount .avatar-1BDn8e,									/* message				container avatar					*/
#app-mount .avatar-2daVqv {									/* message				loading avatar						*/
	position: absolute;
	top: 2px;
	left: calc(-70px * var(--usechatbubbles) + 16px);
}
#app-mount .repliedMessage-VokQwo ~ * .avatar-1BDn8e {
	top: 24px;
}
.container-3FojY8 .avatar-1BDn8e {
	left: calc(-10px * var(--usechatbubbles));
}

#app-mount .replyBadge-r1su3o {								/* message				reply badge							*/
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .spine-1UneWn {
	width: 0px;
	top: 20px;
	right: calc(1px * (-32 * var(--usechatbubbles) + -25 * (1 - var(--usechatbubbles))));
	left: unset;
	border: none;
}
#app-mount .compact-T3H92H .spine-1UneWn {
	right: 0;
}
#app-mount .repliedMessage-VokQwo::before,					/* message				reply spine							*/
#app-mount .repliedMessage-VokQwo::after,
#app-mount .spine-1UneWn::before,							/* message				command spine							*/
#app-mount .spine-1UneWn::after {
	--avatar-size: 40px;
	--gutter: 16px;
	--spine-width: 2px;
	content: "";
	display: block;
	position: absolute;
	-webkit-box-sizing: border-box;
	box-sizing: border-box;
	top: 50%;
	right: unset;
	bottom: 0;
	left: calc(-1*var(--avatar-size) - (6px*var(--usechatbubbles)));
	width: calc(var(--avatar-size) - 4px);
	margin: calc(-1*var(--spine-width)/2) var(--reply-spacing) calc(.125rem - 4px) calc(-1*var(--spine-width)/2);
	border-right: 0 solid var(--background-accent);
	border-left: var(--spine-width) solid var(--background-accent);
}
#app-mount .repliedMessage-VokQwo::before,
#app-mount .repliedMessage-VokQwo::after {
	border-top: var(--spine-width) solid var(--background-accent);
	border-bottom: 0 solid var(--background-accent);
	border-top-left-radius: 6px;
}
#app-mount .spine-1UneWn::before,
#app-mount .spine-1UneWn::after {
	border-top: 0 solid var(--background-accent);
	border-bottom: var(--spine-width) solid var(--background-accent);
	border-bottom-left-radius: 6px;
}
#app-mount .compact-T3H92H .repliedMessage-VokQwo::before,
#app-mount .compact-T3H92H .repliedMessage-VokQwo::after,
#app-mount .compact-T3H92H .spine-1UneWn::before,
#app-mount .compact-T3H92H .spine-1UneWn::after {
	--avatar-size: 20px;
	left: calc(-1*var(--avatar-size));
}
#app-mount .repliedMessage-VokQwo::before,
#app-mount .spine-1UneWn::before {
	border-color: rgba(var(--transparencycolor), calc(0.5 * var(--usechatbubbles)));
}
#app-mount .repliedMessage-VokQwo::after,
#app-mount .spine-1UneWn::after {
	border-color: rgba(var(--textbrighter), calc(0.5 * (1 - var(--usechatbubbles))));
}
#app-mount .compact-T3H92H .repliedMessage-VokQwo::before,
#app-mount .compact-T3H92H .spine-1UneWn::before {
	border-color: transparent;
}
#app-mount .compact-T3H92H .repliedMessage-VokQwo::after,
#app-mount .compact-T3H92H .spine-1UneWn::after {
	border-color: rgba(var(--textbrighter), .3);
}

.cozy-3I4Ja9.content-2Kddbs {								/* message				command content						*/
	background-color: rgba(var(--transparencycolor), .3);
}

.cozy-3raOZG .header-23xsNx::after,							/* message				container header					*/
.cozy-12kSNU .header-1oLBbW::after {						/* message				loading header						*/
	content: "";
	position: absolute;
	top: 12px;
	left: -32px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--transparencycolor), var(--messagetransparency));
}
.cozy-3raOZG .container-3FojY8 .header-23xsNx::after {
	left: 40px;
}
.messageGroupWrapper-o-Zw7G .messageGroupCozy-2iY6cT .header-23xsNx::after {
	top: 2px;
}
.message-1Ng5AR .wrapper-2a6GCs .header-23xsNx::after {
	border-right-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 0.8));
}
.cozy-3raOZG .timestamp-3ZCmNB.alt-1uNpEt {
	left: calc(-78px * var(--usechatbubbles));
}
.cozy-3raOZG .iconContainer-3GkGRf {
	background-color: rgba(var(--transparencycolor), var(--messagetransparency));
	border-radius: 50%;
	left: calc(1px * (-58 * var(--usechatbubbles) + -48 * (1 - var(--usechatbubbles))));
	height: 25px;
	width: 25px;
	margin: unset;
	margin-right: 1rem;
	padding: 0;
}
.cozy-3raOZG .blockedSystemMessage-2Rk1ek .iconContainer-3GkGRf {
	background-color: transparent;
}
.cozy-3raOZG .iconContainer-3GkGRf::after {
	content: "";
	position: absolute;
	top: 2px;
	left: 26px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--transparencycolor), var(--messagetransparency));
}
.cozy-3raOZG .blockedSystemMessage-2Rk1ek .iconContainer-3GkGRf::after {
	display: none;
}
.selected-2P5D_Z.message-2qnXI6.cozy-3raOZG .header-23xsNx::after, 
.mouse-mode .message-2qnXI6.cozy-3raOZG:hover .header-23xsNx::after,
.mouse-mode.full-motion .message-2qnXI6.cozy-3raOZG:hover .header-23xsNx::after,
.mouse-mode .wrapper-1F5TKx.cozy-12kSNU:hover .header-1oLBbW::after,
.mouse-mode.full-motion .wrapper-1F5TKx.cozy-12kSNU:hover .header-1oLBbW::after,
.selected-2P5D_Z.message-2qnXI6.cozy-3raOZG .iconContainer-3GkGRf::after,
.mouse-mode .message-2qnXI6.cozy-3raOZG:hover .iconContainer-3GkGRf::after,
.mouse-mode.full-motion .message-2qnXI6.cozy-3raOZG:hover .iconContainer-3GkGRf::after {
	border-right-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 1.2));
}
#app-mount .ephemeral-1PsL1r.cozy-3raOZG .header-23xsNx::after,
#app-mount .replying-1x3H0T.cozy-3raOZG .header-23xsNx::after,
#app-mount .mentioned-xhSam7.cozy-3raOZG .header-23xsNx::after {
	border-right-color: rgba(var(--accentcolor), calc(var(--messagetransparency) * 100000000000000000000000000000));
}
.message-2DieIs,
.message-2g38UB,
.zalgo-jN1Ica .messageContent-2qWWxC,
.zalgo-jN1Ica.cozy-3raOZG .header-23xsNx,
.wrapper-1F5TKx,
.cozy-12kSNU .header-1oLBbW {
	overflow: visible;
}
.container-3FojY8 {
	padding: 0;
	overflow: visible;
}
#app-mount .cozyMessage-3V1Y8y,								/* message				container cozy						*/
#app-mount .messagesWrapper-1sRNjr .cozy-3raOZG,			/* message				upload placeholder cozy				*/
#app-mount .cozy-12kSNU {									/* message				loading cozy						*/
	margin-left: calc(80px * var(--usechatbubbles));
	padding-left: calc(1px * (10 * var(--usechatbubbles) + 72 * (1 - var(--usechatbubbles))));
}
#app-mount .wrapper-2a6GCs[data-list-item-id*="Uploader"] {
	margin-top: 1rem;
}
#app-mount .compact-3Dy1Ya {								/* message				loading compact						*/
	margin-top: .0625rem;
}
#app-mount .cozy-3raOZG .header-23xsNx,
#app-mount .cozy-3raOZG .messageContent-2qWWxC,
#app-mount .cozy-12kSNU .header-1oLBbW {
	margin-left: 0;
	padding-left: 0;
}
.messageContainer-gbhlwo .wrapper-2a6GCs,
.messages-3G3erD .wrapper-2a6GCs,
.message-2qRu38 .wrapper-2a6GCs,
.messageGroupWrapper-o-Zw7G .messageGroupCozy-2iY6cT,
.message-1Ng5AR .wrapper-2a6GCs {
	border-radius: 5px;
	margin-left: calc(60px * var(--usechatbubbles));
	padding-left: calc(1px * (10 * var(--usechatbubbles) + 72 * (1 - var(--usechatbubbles))));
}
.messages-3G3erD .wrapper-2a6GCs {
	border-radius: 0;
}

.avatar-2daVqv {											/* message				loading avatar						*/
	background: rgba(var(--transparencycolor), .4);
	opacity: 1 !important;
}
.attachment-2p5mHK,											/* message				loading attachment					*/
.blob-2w7iIK {												/* message				loading blob						*/
	background: rgb(var(--accentcolor));
}

.expanded-13sWhZ {											/* message				expanded blocked					*/
	background-color: rgba(var(--transparencycolor), .2);
	border-radius: 5px 5px 0 5px;
	margin-bottom: .5625rem;
}

.reaction-1hd86g {											/* message				reaction							*/
	background-color: rgba(var(--transparencycolor), .3);
	border: none;
}
.reaction-1hd86g:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.reaction-1hd86g.reactionMe-wv5HKu {
	background-color: rgba(var(--accentcolor), .8);
}
.reaction-1hd86g.reactionMe-wv5HKu:hover {
	background-color: rgb(var(--accentcolor));
}
.reaction-1hd86g.reactionMe-wv5HKu .reactionCount-2mvXRV {
	color: #FFF;
	text-shadow: 1px 1px var(--textshadow);
}
.reaction-1hd86g:hover {
	background-color: rgba(var(--transparencycolor), .4);
}

.wrapper-2aW0bm {											/* message				buttons								*/
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	position: relative;
}
.wrapper-2aW0bm::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.button-1ZiXG9:hover {										/* message				button								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.button-1ZiXG9.selected-LCBEAU {
	background-color: rgba(var(--transparencycolor), .4);
}

.bumpBox-1r5p3c {											/* messageelement		publish box							*/
	background-color: rgba(var(--transparencycolor), .4);
}

.markup-2BOw-j code {										/* messageelement		code								*/
	background-color: transparent;
	border-color: transparent;
}
.markup-2BOw-j pre {										/* messageelement		pre									*/
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--transparencycolor), .1);
}
.markup-2BOw-j .inline,										/* messageelement		inline								*/
.after_inlineCode-1KfVgj,
.before_inlineCode-1G9rTK,
.inlineCode-2ngu6Y {
	background-color: rgba(var(--transparencycolor), .4);
}

.textContainer-C0szpm {										/* messageelement 		plain file text						*/
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--transparencycolor), .1);
}
.footer-2yA7Ep {											/* messageelement 		plain file footer					*/
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--transparencycolor), .1);
}
.languageSelector-2LVJrh {									/* messageelement 		plain file popout					*/
	background-color: transparent;
	border: 1px solid rgba(var(--transparencycolor), .3);
	border-radius: 5px;
	box-shadow: 0px 1px 5px 0px rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
.languageSelector-2LVJrh::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	border-radius: 5px;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.languageSelector-2LVJrh::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	border-radius: 5px;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}

#app-mount .spoilerText-3p6IlD {							/* messageelement		spoiler								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .spoilerText-3p6IlD.hidden-HHr2R9 {				/* messageelement		hiddenspoiler						*/
	background-color: rgba(var(--transparencycolor), .5);
}

.icon-2Po-VO[style*="/assets/5da4cdab01d4d89c593c48c62ae0d937.svg"] {		/* systemmessage			pinicon									*/
	-webkit-mask: url(https://discord.com/assets/5da4cdab01d4d89c593c48c62ae0d937.svg) center/cover no-repeat;
	background: var(--channels-default) !important;
}
.icon-2Po-VO[style*="/assets/d80d1fdc43a3c42134a31a39581160ac.svg"] {		/* systemmessage			missedcall								*/
	-webkit-mask: url(https://discord.com/assets/d80d1fdc43a3c42134a31a39581160ac.svg) center/cover no-repeat;
	background: var(--channels-default) !important;
}
.icon-2Po-VO[style*="/assets/b8029fe196b8f1382e90bbe81dab50dc.svg"] {		/* systemmessage			joincallicon							*/
	-webkit-mask: url(https://discord.com/assets/b8029fe196b8f1382e90bbe81dab50dc.svg) center/cover no-repeat;
	background: rgb(var(--accentcolor)) !important;
}
.icon-2Po-VO[style*="/assets/c30220457097b064286a8759a9b6c4af.svg"] {		/* systemmessage			recievecallicon							*/
	-webkit-mask: url(https://discord.com/assets/c30220457097b064286a8759a9b6c4af.svg) center/cover no-repeat;
	background: rgb(var(--accentcolor)) !important;
}

/* ====		6.2.2.	EMBEDS							==== */

#app-mount .embedFull-2tM8-- {								/* embed				wrapper								*/
	background-color: rgba(var(--transparencycolor), .3);
	border-left-color: rgb(var(--textdarkest));
}

#app-mount .attachment-33OFj0 {								/* attachment			container							*/
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
	margin-left: 18px;
}
#app-mount .message-2qnXI6 .attachment-33OFj0 {
	margin-left: 0;
}
#app-mount .twitchSectionPlayButton-2RamGG {
	object-position: -999999px -999999px;
	background: rgba(var(--transparencycolor), .4) url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none"><path d="M12.3333 10.002V22.002L22.3333 16.002L12.3333 10.002Z" fill="rgb(185,187,190)"/></svg>');
	border-radius: 50%;
}
#app-mount .twitchSectionPlayButton-2RamGG:hover {
	background-color: rgba(var(--transparencycolor), .8);
}

#app-mount .wrapper-2TxpI8 {								/* attachment			videowrapper						*/
	background-color: rgba(var(--transparencycolor), .3);
}

/* ====		6.2.3.	NITROGIFT						==== */

#app-mount .tile-2OwFgW {									/* gift					container							*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 0 0 rgba(var(--transparencycolor), .15);
}
#app-mount .tile-2OwFgW:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .title-1rUb9I {									/* gift					title								*/
	color: var(--header-primary);
}
#app-mount .description-1RsfgZ {							/* gift					description							*/
	color: var(--header-primary);
}
#app-mount .tagline-2nvxi0 {								/* gift					tagline								*/
	color: var(--header-secondary);
}

/* ====		6.2.4.	INVITE							==== */

#app-mount .wrapper-35wsBm {								/* invite				container							*/
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .guildIconImage-3qTk45 {							/* invite				icon								*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .guildName-2hvnt_ {								/* invite				name								*/
	color: var(--header-primary);
}
#app-mount .guildDetail-1nRKNE {							/* invite				details								*/
	color: var(--channels-default);
}

#app-mount .invite-18yqGF {									/* invite				group invite						*/
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .header-Hg_qNF {
	color: rgb(var(--textdarker));
}
#app-mount .name-GG2Mcs,
#app-mount .partyStatus-6AjDud {
	color: var(--header-primary);
}
#app-mount .moreUsers-1sZP3U {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .partyMemberEmpty-2iyh5g {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .helpIcon-2EyVTp {
	background-color: var(--header-primary);
}


/* ----		6.3.	TEXTAREA						---- */

.form-2fGMdU {
	padding-top: 0;
	margin-top: 0;
}
.form-2fGMdU {												/* textarea				form								*/
	background: rgba(var(--transparencycolor), var(--chatinputtransparency));
	margin-top: 0;
	padding-top: 8px;
	border-top-right-radius: calc(8px * (1 - (var(--memberlisttransparency) / (var(--memberlisttransparency) + 0.00000000000000000000001))));
	border-top-left-radius: calc(8px * (1 - (var(--guildchanneltransparency) / (var(--guildchanneltransparency) + 0.00000000000000000000001))));
}
.form-2fGMdU::before {
	display: none;
}

.channelTextArea-rNsIhG {									/* textarea				channeltextarea						*/
	background-color: transparent;
	border-top-color: var(--background-modifier-accent);
}

.container-2fRDfG {											/* textarea				reply								*/
	background: rgba(var(--transparencycolor), .3);
	border: none;
	border-bottom: 1px solid var(--background-modifier-accent);
}

.scrollableContainer-2NUZem {								/* textarea				container							*/
	background-color: rgba(var(--transparencycolor), .3);
}

.sprite-2iCowe {											/* textarea				emojibutton							*/
	transform: none !important;
}

.wrapper-39oAo3 {											/* textarea				placeholder							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--text-normal);
}

.toolbar-2bjZV7 {											/* textarea				formattoolbar						*/
	background-color: rgb(var(--accentcolor));
}
.toolbar-2bjZV7::before {
	border-top-color: rgb(var(--accentcolor));
}
.divider-24xeUg {											/* textarea				formattoolbar divider				*/
	border-left-color: hsla(0, 0%,100%, .1);
}
.active-2HPddW,												/* textarea				buttonactive						*/
.hover-28QbSq:hover {										/* textarea				buttonhover							*/
	background-color: hsla(0, 0%, 100%, .2);
}
.icon-KgGMGo {												/* textarea				buttonicon							*/
	color: #fff;
	opacity: .7;
}
.active-2HPddW .icon-KgGMGo,
.hover-28QbSq:hover .icon-KgGMGo {
	color: #fff;
	opacity: 1;
}

#app-mount .pill-2pQByF {									/* textarea				command query pill					*/
	background-color: rgba(var(--transparencycolor), .5);
	border-radius: 5px;
}

/* ----		6.4.	AUTOCOMPLETEMENU				---- */

#app-mount .autocomplete-1vrmpx {							/* autocomplete			container							*/
	background-color: transparent;
	overflow: hidden;
}
#app-mount .autocomplete-1vrmpx::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .autocomplete-1vrmpx::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.theme-brand .autocomplete-1vrmpx {
	background: rgb(var(--accentcolor)) linear-gradient(rgba(var(--transparencycolor), .2), rgba(var(--transparencycolor), .2)) !important;
}
.theme-brand .autocomplete-1vrmpx::before,
.theme-brand .autocomplete-1vrmpx::after {
	display: none;
}
#app-mount .bar-AokMp3 {									/* autocomplete			command info						*/
	background-color: transparent;
}
#app-mount .container-3ISnnM::after {
	box-shadow: inset 0 -7px 12px -7px rgba(var(--transparencycolor), .3);
}
#app-mount .header-1TOWci {									/* autocomplete			header								*/
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor), .2), 0 1px 2px 0 rgba(var(--transparencycolor), .2);
}
#app-mount .selected-1Tbx07 {								/* autocomplete			rowselected							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .option-1B5ZV8 {									/* autocomplete			option								*/
	background-color: rgba(var(--transparencycolor), .5);
}

#app-mount .wrapper-uf3cnO {								/* autocomplete			categories							*/
	background-color: transparent;
}
#app-mount .selected-3xBBKs,								/* autocomplete			category selected					*/
#app-mount .selected-3xBBKs:hover {
	background-color: rgb(var(--accentcolor));
}
#app-mount .selected-3xBBKs svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

#app-mount .searchSuggestion-2K8OBX:hover {					/* gifpicker			suggestions							*/
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .placeholder-1kJjXI {							/* gifpicker			result placeholder					*/
	background-color: rgba(var(--transparencycolor), .3);
}

/* ----		6.5.	MEMBERLIST						---- */

.member-3-YXUe:hover .layout-2DM8Md {						/* member				inner								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.selected-aXhQR6.member-3-YXUe .layout-2DM8Md {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.selected-aXhQR6.member-3-YXUe .layout-2DM8Md svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.member-3-YXUe.selected-aXhQR6 .premiumIcon-2IFPOX {
	color: var(--header-primary) !important;
}

.avatar-VxgULZ::before {									/* emptyavatar												*/
	background-color: rgba(var(--transparencycolor), .3);
}

.memberGroupsPlaceholder-3mwPub,							/* loadingplaceholders										*/
.placeholderAvatar-damqh6,
.placeholderUsername-2B_OA9 {
	background-color: rgba(var(--transparencycolor), .4);
}

/* ----		6.6.	SEARCHPAGE						---- */

.searchResultsWrap-3-pOjs {									/* searchpage			container							*/
	background-color: transparent;
}
.searchHeader-2XoQg7 {										/* searchpage			header								*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
	border-radius: 0 0 0 8px;
}
#app-mount .tab-2j5AEF.selected-2LAck8 {					/* searchpage			selected tab						*/
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.channelName-1JRO3C {										/* searchpage			channelname							*/
	background-color: transparent;
}
.searchResult-9tQ1uo {										/* searchpage			searchresult						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.button-11zvza {											/* searchpage			jumpbutton							*/ 
	background-color: rgba(var(--transparencycolor), .4);
}
.button-11zvza:hover {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.pageButton-2ruNwd:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.activeButton-rvKcqq {
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		6.7.	CALL							---- */

#app-mount .root-3JVdIJ {									/* popout				inner								*/
	background-color: transparent;
	border: none;
}
.root-3JVdIJ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.root-3JVdIJ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .wrapper-2qzCYF {								/* call					voice wrapper					*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
}
#app-mount .root-217Brm {									/* call					root							*/
	color: var(--header-primary);
}
.videoWrapper-2v09vt {										/* call					video wrapper					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.video-1FfuMD {												/* call					video							*/
	background-color: transparent;
}
.tile-2naSqK,												/* call					user video voicechannel			*/
.tile-2gi3tr {												/* call					user video dm					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.gradientContainer-10lXLB {									/* call					gradientcontainer				*/
	display: none;
}
.participantsButton-KYW-IW {								/* call					participantsbutton				*/
	background-color: rgba(0, 0, 0, .3);
}
.participantsButton-KYW-IW:hover {
	background-color: rgba(0, 0, 0, .6);
}
.centerButton-3CaNcJ,
.colorable-1bkp8v.primaryDark-3mSFDl {
	background-color: rgba(var(--transparencycolor), .5);
}
.centerButton-3CaNcJ:hover,
.colorable-1bkp8v.primaryDark-3mSFDl:hover {
	background-color: rgb(var(--accentcolor));
}
.button-3HqqDX {
	background-color: rgba(var(--transparencycolor), .4);
}
.button-3HqqDX:hover {
	background-color: rgba(var(--transparencycolor), .6);
}
.controlButton-2MhVEL.leaveButton-2YnTyt {
	background-color: rgba(var(--dangercolor)),.5);
}
.controlButton-2MhVEL.leaveButton-2YnTyt:hover {
	background-color: rgb(var(--dangercolor));
}
.regionSelectPopout-p9-0_W {
	width: 170px;
}

.container-pTf0Ly {											/* call					podium wrapper					*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
}
.callContainer-3UuV6S {										/* call					podium inner					*/
	background-color: transparent;
}
.scroller-1SuHJo {											/* call					podium scroller					*/
	background-color: transparent;
}
.container-2t1JyW {											/* call					podium info						*/
	background-color: transparent;
}
.rowContainer-2tYerQ {										/* call					podium row						*/
	background-color: transparent;
}
.participants-soO0aD {										/* call					podium participants				*/
	background-color: transparent;
}
.tileContainer-BaRAZF:hover {								/* call					podium participant				*/
	background-color: rgb(var(--accentcolor));
}
.container-1EOCj2 {											/* call					podium requests					*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.3));
}
.headerContainer-3Dbfbk {									/* call					podium requests header			*/
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
}

/* ----		6.8.	UNAVAILABLESCREEN				---- */

.category-2haXBH,											/* loadingplaceholders										*/
.channelIcon-1TvDoP,
.channelName-2wrHHc {
	background: rgba(var(--transparencycolor), .4);
}
.splashImage-13vBzp {										/* screen				image								*/
	opacity: 0.7;
}


/* ~~~~		7.		PEOPLES							~~~~ */

.wrapper-1cBijl {											/* friendsadd			inputcontainer						*/
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
.wrapper-1cBijl:hover {
	border-color: rgb(var(--transparencycolor));
}

.peopleListItem-2nzedh .actionButton-uPB8Fs {				/* peoples				actionbutton						*/
	background-color: rgba(var(--transparencycolor), .1);
}
.peopleListItem-2nzedh .actionButton-uPB8Fs:hover {
	background-color: rgb(var(--accentcolor));
}
.peopleListItem-2nzedh .actionButton-uPB8Fs:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.peopleListItem-2nzedh.active-rhSpJJ,
.peopleListItem-2nzedh:hover {
	background-color: rgba(var(--transparencycolor), .3);
}
.peopleListItem-2nzedh.active-rhSpJJ .actionButton-uPB8Fs,
.peopleListItem-2nzedh:hover .actionButton-uPB8Fs {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .outer-1AjyKL {									/* playing				card								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .outer-1AjyKL.active-1xchHY,
#app-mount .outer-1AjyKL.interactive-3B9GmY:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .inset-3sAvek {									/* playing				card inner							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.emptyCard-1RJw8n {											/* playing				empty card							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .partyMemberOverflow-lXnzvu {
	background: rgba(var(--transparencycolor), .5);
}
#app-mount .partyMemberBackground-3XOgDv,
#app-mount .partyMemberUnknown-fwK2DC {
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .partyMemberUnknownIcon-1eDbV6 {
	color: var(--channels-default);
}
#app-mount .popout-38lTFE {									/* playing				popout								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 8px 16px 0 rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
.popout-38lTFE::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-38lTFE::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.3));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .memberListItem-31QoHj:not(.popoutDisabled-2RK7MF):hover,
#app-mount .enabled-1t_Gxm:hover {
	background-color: rgba(var(--transparencycolor), .2);
}


/* ~~~~		7.		STORE/NITRO						~~~~ */

.gridItemBadge-1Se-Pu {
	text-shadow: 1px 1px var(--textshadow);
}

.marketingHeader-2Iq7qk {									/* marketingheader											*/
	background-color: rgba(var(--transparencycolor), .3);
}

.detailsBlock-FoDTGA {										/* billing 				details								*/
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .categoryHeader-1D7Tqy,							/* categoryheader											*/
#app-mount .premiumApplicationsHeader-Zmkm5e {
	border-color: var(--background-modifier-accent);
	color: var(--header-primary);
}

#app-mount .tier1Banner-1BTgv0 {							/* tier1banner			container							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: #fff;
}
.headerIcon-3bqya6 {										/* tier1banner			svgtitle							*/
	color: #fff;
}

.smallCarousel-2e0IQc {
	background-color: rgba(var(--transparencycolor), .3);
	border-radius: 5px;
}
#app-mount .item-3V15ea {									/* gamepreview			previewitem							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.arrow-3jRqK8 {												/* gamepreview			prev/nextarrow (big)				*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .themedPagination-3v0Dnu .arrow-vOpU7R {			/* gamepreview			prev/nextarrow (small)				*/
	color: var(--header-primary);
}
#app-mount .themedPagination-3v0Dnu .dot-2Q_mMZ {			/* gamepreview			itemdot (small)						*/
	background-color: var(--header-primary);
}

#app-mount .root-1bFE0x {									/* gameinfo				sectioncontainer					*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .header-3HFF3R {									/* gameinfo				sectionheader						*/
	color: var(--header-primary);
}
#app-mount .section-7tu4tu {								/* gameinfo				subsection							*/
	border-bottom-color: var(--background-modifier-accent);
}
#app-mount .playerOverflow-2Hf77M {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .description-2Ifi6N {							/* gameinfo				subsectiondescription				*/
	color: var(--header-secondary);
}
#app-mount .description-2Ifi6N strong,
#app-mount .username-2gp_Xw {								/* gameinfo				subsectionusername					*/
	color: var(--header-primary);
}
#app-mount .smallHeader-2h-9-U {							/* gameinfo				subsectionheader					*/
	color: var(--header-secondary);
}
#app-mount .text-1Z3P6i {									/* gameinfo				subsectiontext						*/
	color: var(--header-primary);
}
#app-mount .iconCircle-1dlYo0 {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .circle-1nK_79 {
	color: var(--header-primary);
}

#app-mount .divider-21LyPb {								/* section				divider								*/
	border-color: var(--background-modifier-accent);
}
#app-mount .blurb-1iBKJy {									/* section				description							*/
	color: var(--text-normal);
}
#app-mount .description-1AwRKJ {							/* section				subdescription						*/
	color: var(--header-secondary);
}

#app-mount .requirements-dEriwm {							/* requirements												*/
	color: var(--text-normal);
}
#app-mount .requirementKey-14DT2D {							/* requirements			key									*/
	color: rgb(var(--textdarker));
}
#app-mount .content-1zhNsr {								/* requirements			rating								*/
	color: rgb(var(--textdarker));
}
#app-mount .content-3FEARf {								/* requirements			copyright							*/
	color: rgb(var(--textdarker));
}

#app-mount .bodySection-jqkkIP {							/* sidebar				section								*/
	background-color: rgba(var(--transparencycolor), .2);
	border-top-color: var(--background-modifier-accent);
}
#app-mount .actionText-3EKWER {								/* sidebar				header								*/
	color: var(--text-normal);
}
#app-mount .purchaseUnitOperatingSystem-cnbJPz {			/* sidebar				OSicon								*/
	color: rgb(var(--textdarkest));
}
#app-mount .price-4PDWNj,									/* sidebar				price								*/
#app-mount .listingPrice-2GiDSc {
	color: var(--header-primary);
}
#app-mount .title-2xCQKy {									/* sidebar				subtitle							*/
	color: var(--header-primary);
}
#app-mount .skuNormal-3h1es- {								/* sidebar				pricerow							*/
	border-bottom-color: var(--background-modifier-accent);
}
#app-mount .name-u2zgy7 {									/* sidebar				pricename							*/
	color: var(--header-secondary);
}
#app-mount .sku-epQEb_:hover .name-u2zgy7 {
	color: var(--header-primary);
}
#app-mount .price-NUANu6 {									/* sidebar				priceamount							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .label-13UUcd {									/* sidebar				label								*/
	color: rgb(var(--textdarker));
}
#app-mount .info-1Emy1X {									/* sidebar				labelinfo							*/
	color: var(--header-primary);
}

#app-mount .content-35aVm0 {								/* invitecard			container							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .name-3TBxUq {									/* invitecard			guildname							*/
	color: var(--header-secondary);
}
#app-mount .memberInfo-1TAaKC {								/* invitecard			memberinfo							*/
	color: rgb(var(--textdarker));
}

.premiumSubscriptionAccountCredit-25i0tQ {					/* abonnements			abocard								*/
	background-color: rgba(var(--transparencycolor), .4);
}

#app-mount .row-1bU71H {									/* features				row									*/
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-secondary);
}
#app-mount .featureIcon-1f78KU {							/* features				featureicon							*/
	color: var(--header-secondary);
}
#app-mount .feature-2w65J5 {								/* features				feature								*/
	background-color: rgba(var(--transparencycolor), .4);
}
.featureImage-2L9kA0 {										/* features				image								*/
	opacity: 0.7;
}
.banner-WELp4M {											/* features				xbox promo							*/
	background-color: rgba(var(--transparencycolor), .4);
}


/* ~~~~		9.		LIBRARY							~~~~ */

.header-39GIC8 {											/* library				table header						*/
	background-color: transparent;
	border-bottom-color: var(--background-modifier-accent);
	position: relative;
}
.header-39GIC8::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.header-39GIC8::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), .4);
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .headerCellSorted-1JR4Ny {
	color: var(--header-primary);
}

.rowWrapperActive-2L7i9f {
	background-color: rgba(var(--transparencycolor), .2);
}
.rowWrapper-2fB6P0 + .rowWrapper-2fB6P0 .row-ZLfFhY {
	border-top-color: var(--background-modifier-accent);
}

#app-mount .rate-1Gat8e {
	color: var(--text-muted);
}
#app-mount .background-yZEZik {								/* library				usagebar							*/
	stroke: rgb(var(--transparencycolor), .5);
}
#app-mount .usageInfo-2WQAwr {								/* gamelibrary			usageinfo							*/
	color: var(--header-secondary);
}

#app-mount .installationPath-3cStrB {						/* library				game row path						*/
	box-shadow: 0 1px 0 0 var(--background-accent);
}
#app-mount .rowTitle-1KYtY7 {								/* library				game row title						*/
	color: var(--text-normal);
}
#app-mount .rowBody-3dJTTZ {								/* library				game row body						*/
	color: var(--text-muted);
}
#app-mount .defaultLocationCheckbox-3HMIPO {				/* library				location checkbox					*/
	color: var(--header-primary);
}
#app-mount .defaultIndicator-3WqGFB {						/* library				location indicator					*/
	background-color: rgba(var(--transparencycolor), .5);
	color: var(--header-primary);
}

#app-mount .applicationName-2toV6z {						/* library				application name					*/
	color: var(--header-primary);
}
#app-mount .applicationSubText-2V8LSK {						/* library				application subtext					*/
	color: var(--text-muted);
}

#app-mount .emptyWumpus-12J3jI {							/* library				no games							*/
	background: url(https://discord.com/assets/131dcaaa628405e6d0ebee7708111c7a.svg);
	opacity: 0.6;
}


/* ~~~~		10.		DISCOVERY						~~~~ */

.categoryItem-1QIroW:hover .itemInner-gPkiWb{				/* guilddiscovery		categoryitem						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.categoryItem-1QIroW.selectedCategoryItem-FHKU_o .itemInner-gPkiWb {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.categoryItem-1QIroW.selectedCategoryItem-FHKU_o .itemInner-gPkiWb svg:not(.svg-2V3M55) {
	filter: drop-shadow(1px 1px var(--textshadow));
}

#app-mount .pageWrapper-1PgVDX {							/* guilddiscovery		container							*/
	color: var(--header-primary);
}
#app-mount .card-3DjzTQ {									/* guildcard			container							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .iconMask-3b8GzQ {								/* guildcard			iconmask							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .card-3DjzTQ:hover,
#app-mount .iconMask-3b8GzQ:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .cardPlaceholder-1zrbbe {						/* guildcard			placeholder							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .loading-17PYl_ {								/* guildcard			loading								*/
	background-color: rgba(var(--transparencycolor), .5);
}

.emojiContainer-1u-_sQ {									/* search				emojicontainer						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.emptyContainer-1_gwCl {									/* search				no results							*/
	background-color: rgba(var(--transparencycolor), .4);
}
.placeholder-2erB-x {										/* search				placeholder							*/
	background-color: rgba(var(--transparencycolor), .4);
}


/* ~~~~		11.		USERSETTINGS					~~~~ */

.premiumTabItem-1QTfBr[aria-selected=true],
.item-PXvHYJ.selected-3s45Ha[aria-controls="Nitro Server Boost-tab"],
.serverBoostTabItem-2hFTIN[aria-selected=true] {
	text-shadow: 1px 1px var(--textshadow);
}
.side-8zPYf6 .themed-OHr7kt.item-PXvHYJ:hover:not(.disabled-1Hwwfb),		/*		sideitems							*/
.topPill-30KHOu .themed-OHr7kt.item-PXvHYJ:hover:not(.disabled-1Hwwfb) {	/*		tabitems							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.side-8zPYf6 .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ,
.topPill-30KHOu .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ,
.side-8zPYf6 .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ:hover,
.topPill-30KHOu .themed-OHr7kt.selected-3s45Ha.item-PXvHYJ:hover {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .foreground-26ym5y {								/* sidebar				sideitemlink						*/
	background: var(--interactive-normal);
}
#app-mount .link-1IoFq-:hover .foreground-26ym5y {
	background: var(--interactive-active);
}

.bd-social-link[title="BD" i] .bd-social-logo,
.bd-social-link[title="BetterDiscord" i] .bd-social-logo,
.bd-social-link[title="BBD" i] .bd-social-logo,
.bd-social-link[title="BandagedBD" i] .bd-social-logo {
	background: var(--interactive-normal);
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/settingsicons/betterdiscord.svg) center/contain no-repeat;
	opacity: 1;
	transition: background .15s ease;
}
.bd-social-link[title="BD" i]:hover .bd-social-logo,
.bd-social-link[title="BetterDiscord" i]:hover .bd-social-logo,
.bd-social-link[title="BBD" i]:hover .bd-social-logo,
.bd-social-link[title="BandagedBD" i]:hover .bd-social-logo {
	background: var(--interactive-active);
}
.bd-social-link[title="BD" i] .bd-social-logo > *,
.bd-social-link[title="BetterDiscord" i] .bd-social-logo > *,
.bd-social-link[title="BBD" i] .bd-social-logo > *,
.bd-social-link[title="BandagedBD" i] .bd-social-logo > * {
	display: none;
}

.contentRegion-3nDuYy div[role="tabpanel"] {				/* tabpanel													*/
	width: 100%;
}
.toolsContainer-1edPuj {									/* closebutton			wrapper								*/
	margin-right: 37px;
}
#app-mount .closeButton-1tv5uR {							/* closebutton			button								*/
	border-color: var(--channels-default);
}
#app-mount .closeButton-1tv5uR path[fill] {
	fill: var(--channels-default);
}
#app-mount .closeButton-1tv5uR:hover {
	background-color: rgba(var(--accentcolor), .2);
	border-color: var(--header-secondary);
}
#app-mount .closeButton-1tv5uR:hover path[fill] {
	fill: var(--header-secondary);
}
#app-mount .closeButton-1tv5uR:active {
	border-color: var(--text-normal);
}
#app-mount .closeButton-1tv5uR:active path[fill] {
	fill: var(--text-normal);
}
#app-mount .keybind-KpFkfr {								/* closebutton			keybind								*/
	color: var(--channels-default);
}

#app-mount .closeButtonBold-8kKURP {						/* closebutton			button bold							*/
	border-color: var(--header-secondary);
}
#app-mount .closeButtonBold-8kKURP path[fill] {
	fill: var(--header-secondary);
}
#app-mount .closeButtonBold-8kKURP:hover {
	background-color: rgba(var(--accentcolor), .4);
	border-color: var(--text-normal);
}
#app-mount .closeButtonBold-8kKURP:hover path[fill] {
	fill: var(--text-normal);
}
#app-mount .closeButtonBold-8kKURP:active {
	border-color: var(--header-primary);
}
#app-mount .closeButtonBold-8kKURP:active path[fill] {
	fill: var(--header-primary);
}
#app-mount .keybindBold-1942Wp {							/* closebutton			keybind bold						*/
	color: var(--header-secondary);
}

.cardPrimary-1Hv-to, .cardPrimaryEditable-3KtE4g {			/* settingsitems		card								*/
	border-color: rgba(var(--transparencycolor), .1);
}
.cardPrimary-1Hv-to {
	background-color: rgba(var(--transparencycolor), .2);
}
.cardPrimaryEditable-3KtE4g {
	background-color: rgba(var(--transparencycolor), .1);
}
.cardPrimaryOutline-29Ujqw {
	border-color: rgba(var(--transparencycolor), .2);
}

.questionMark-3qBhGj svg {									/* accountsettings		questionmark new					*/
	filter: drop-shadow(1px 1px var(--textshadow));
}
#app-mount .avatarUploader-3XDtmn .removeButton-1hcZyG {	/* accountsettings		removeavatar						*/
	color: var(--header-secondary);
}
#app-mount .avatarUploader-3XDtmn .removeButton-1hcZyG:hover {
	color: var(--text-muted);
}
#app-mount .userSettingsSecurity-3IYeMF .codeCheckbox-1T0TTy {
	color: var(--text-normal);
}
#app-mount .background-1QDuV2 {								/* accountsettings		container							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .fieldList-21DyL8 {								/* accountsettings		settings							*/
	background-color: rgba(var(--transparencycolor), .4);
}

.accountList-33MS45 {										/* connections			container							*/
	background-color: rgba(var(--transparencycolor), .4);
}
.accountBtn-2Nozo3 .accountBtnInner-sj5jLs {				/* connections			connectioninner						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.accountBtn-2Nozo3 .accountBtnInner-sj5jLs:hover {
	background-color: rgb(var(--accentcolor));
}
.connection-1fbD7X {										/* connections			connection							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.connectionHeader-2MDqhu {									/* connections			connection header					*/
	background-color: rgba(var(--transparencycolor), .2);
}

.guildHeader-3nh5RK {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--transparencycolor), .5);
}
.guildSubscriptionSlots-JPXXvN {							/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.cardWrapper-2Min21 {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.cardWrapper-2Min21:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.cardWrapper-2Min21 .card-3AyPWq,							/* boostsettings		suggestioncard inner				*/
.cardWrapper-2Min21 .card-3AyPWq:hover {
	background-color: transparent;
}
#app-mount .gemIndicatorContainer-2jdECl {					/* boostsettings		suggestioncard circle				*/
	background-color: transparent;
}
#app-mount .summaryInfo-2QFKUg {							/* boostsettings		past transactions summary			*/
	color: var(--header-primary);
}
#app-mount .payment-xT17Mq {								/* boostsettings		past transactions payment			*/
	background-color: transparent;
	color: var(--header-secondary);
}
#app-mount .hoverablePayment-Yc6mK7:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .paymentHeader-3QlZQi {							/* boostsettings		past transactions header			*/
	color: var(--header-primary);
	border-color: var(--background-modifier-accent);
}
#app-mount .expandedInfo-3kfShd {							/* boostsettings		past transactions expandedinfo		*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .paymentText-2vaF7U {							/* boostsettings		past transactions paymenttext		*/
	color: var(--header-secondary);
}
#app-mount .giftIcon-3DRGI6 {								/* boostsettings		past transactions gifticon			*/
	color: var(--header-primary);
}

#app-mount .paymentPane-3bwJ6A {							/* boostsettings		past transactions					*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .paginator-166-09 {								/* boostsettings		past transactions paginator			*/
	background: rgba(var(--transparencycolor), .3);
	color: var(--text-muted);
}
#app-mount .bottomDivider-1K9Gao {							/* boostsettings		past transactions divider			*/
	border-bottom-color: rgba(var(--transparencycolor), .3);
}
#app-mount .tab-1kx2RU {									/* boostsettings		past transactions tab				*/
	color: var(--text-muted);
}
#app-mount .externalRowHeader-2-8cG6 {						/* boostsettings		past transactions extenal row		*/
	color: var(--header-secondary);
}

.emptyStateImage-2MrSNs {									/* giftinventory		no gifts							*/
	opacity: 0.6;
}

#app-mount .codeRedemptionRedirect-1wVR4b {					/* payment				coderedem							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
	color: var(--header-primary);
}

.membershipDialogHouse1-3KhKE- {							/* hypesquad			membershipdialogs					*/
	background-color: rgba(156, 132, 239, .8);
}
.membershipDialogHouse2-35h9SY {
	background-color: rgba(244, 123, 103, .8);
}
.membershipDialogHouse3-15OBIQ {
	background-color: rgba(69, 221, 192, .8);
}
.videoWrapper-3YdgHH {
	background-color: rgba(var(--transparencycolor), .4);
}

.container-3PXSwK {											/* voicesettings		voicebarcontainer					*/
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/voice_level_bar.svg);
}
.notches-1sAcEM {
	background: transparent !important;
}
#app-mount .progress-1IcQ3A {								/* voicesettings		voicebar							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.icon-4lJsMQ[src="/assets/ebfb23f0cdb11b1871ed8beb3f9ec0ee.svg"],
.icon-4lJsMQ[src="/assets/c28317e203e00b2d7390d5ece2399228.svg"] {
	-webkit-mask: url(https://discord.com/assets/c28317e203e00b2d7390d5ece2399228.svg) center/contain no-repeat;
	background-color: var(--header-primary);
	object-position: -999999px -999999px;
}
.icon-4lJsMQ[src="/assets/8c49c7d4a59675bb6ceaee1bb80b5803.png"],
.icon-4lJsMQ[src="/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png"] {
	-webkit-mask: url(https://discord.com/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png) center/contain no-repeat;
	background-color: var(--header-primary);
	object-position: -999999px -999999px;
}
.userSettingsVoice-iwdUCU .media-engine-video {				/* voicesettings		video								*/
	background: transparent;
}
#app-mount .userSettingsVoice-iwdUCU .previewOverlay-2O7_KC {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
}

.option-n0icdO {											/* overlay				option								*/
	background-color: rgba(var(--transparencycolor), .4);
}
.option-n0icdO:hover,
.option-n0icdO.selected-mKYnfr {
	box-shadow: 0 2px 0 rgba(var(--transparencycolor), .3);
}
.disabled-3I9jyo {
	color: rgba(var(--transparencycolor), .4);
}

#app-mount .row-2okwlC {									/* hotkeys				row									*/
	box-shadow: inset 0 -1px 0 var(--background-modifier-accent);
}

#app-mount .card-FDVird::before {							/* settingscard			backdrop							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .button-2CgfFz {									/* settingscard			removebutton						*/
	background-color: rgba(var(--transparencycolor), .3);
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .6), 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .button-2CgfFz:hover {
	background-color: rgba(var(--transparencycolor), .7);
}

#app-mount .game-1ipmAa {									/* games				card								*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
#app-mount .gameNameInput-385LoS:focus,
#app-mount .gameNameInput-385LoS:hover {
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .gameName-1RiWHm {								/* games				gamename							*/
	color: var(--header-primary);
}
#app-mount .lastPlayed-3bQ7Bo,								/* games				lastplayed							*/
#app-mount .overlayStatusText-L2IACa {						/* games				overlaystatustext					*/
	color: var(--text-muted);
}
#app-mount .overlayToggleIconOn-3UNmty .fill-1ugeBG {		/* games				overlaystatusicon					*/
	fill: var(--text-muted);
}
#app-mount .nowPlayingAdd-1Kdmh_ {							/* games				descriptionhint						*/
	color: var(--header-secondary);
}
#app-mount .nowPlaying-284llR .gameName-1RiWHm {
	color: #fff;
}
#app-mount .nowPlaying-284llR .lastPlayed-3bQ7Bo,
#app-mount .nowPlaying-284llR .overlayStatusText-L2IACa {
	color: #b4e1cd;
}
#app-mount .nowPlaying-284llR .overlayToggleIconOff-1kT42w .fill-1ugeBG,
#app-mount .nowPlaying-284llR .overlayToggleIconOn-3UNmty .fill-1ugeBG {
	fill: #b4e1cd;
}
#app-mount .notDetected-33MY4s {							/* games				nogame								*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .notDetected-33MY4s .lastPlayed-3bQ7Bo {
	color: var(--header-secondary);
}
#app-mount .activeGame-14JI7o .removeGame-2JFGPn {
	background-image: none;
}
#app-mount .activeGame-14JI7o .removeGame-2JFGPn::after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: var(--header-primary);
	-webkit-mask: url(https://discord.com/assets/eb69ec9fdd30653a3ade1ab501a7cd3d.svg) center no-repeat;
}

#app-mount .addGamePopout-2RY8Ju {							/* games				add game popout						*/
	background-color: transparent;
}
.addGamePopout-2RY8Ju::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.addGamePopout-2RY8Ju::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.15));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .addGamePopout-2RY8Ju .cancelButton-10XRsm {
	color: var(--header-primary);
}

.preview-2nSL_2 {											/* appearance			preview								*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .2);
}

#app-mount .item-3eFBNF {									/* languagesettings		row									*/
	border-radius: 5px;
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
.item-3eFBNF:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.item-3eFBNF.selected-2DeaDa {
	background-color: rgba(var(--transparencycolor), .4);
}


/* ~~~~		12.		GUILDSETTINGS					~~~~ */

.container-2VW0UT {											/* settings				confirmnotice						*/
	position: relative;
}
.container-2VW0UT[style*="background-color: rgba(248, 249, 249"],
.container-2VW0UT[style*="background-color: rgba(32, 34, 37"] {
	background-color: rgba(var(--transparencycolor), .7) !important;
}
.container-2VW0UT::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
	pointer-events: none;
	z-index: -1;
}

.roles-1ti6KV {												/* rolesettings			intro roles							*/
	z-index: 2;
}
.profileCard-2RGvbu {										/* rolesettings			intro profile						*/
	position: relative;
	z-index: 1;
}
.profileCard-2RGvbu::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.sidebar-dLM-kh {											/* rolesettings			sidebar								*/
	background-color: rgba(var(--transparencycolor), .1);
	border: none;
}
.container-_phMUq {											/* rolesettings			everyone role						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.container-_phMUq:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
img[src="/assets/cef02719c12d8aaf38894c16dca7fbe6.svg"] {	/* rolesettings			addrolebutton						*/
	-webkit-mask: url(https://discord.com/assets/cef02719c12d8aaf38894c16dca7fbe6.svg);
	background: currentColor;
	object-position: -999999px -999999px;
}
.settingCard-3w2mVL {										/* rolesettings			setting card						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.settingCard-3w2mVL.active-1ytUzX {							/* rolesettings			setting card active					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.cardContent-qqqwo8 {										/* rolesettings			setting card header					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.cardFolder-28dwxo {										/* rolesettings			setting card body					*/
	background-color: transparent;
}
.group-1WdBVp {												/* rolesettings			permissions group					*/
	border-color: rgb(var(--transparencycolor), .4);
}
.item-1yAxl1 {												/* rolesettings			permissions item					*/
	background: rgb(var(--transparencycolor), .2);
}
.item-1yAxl1:hover {
	background: rgb(var(--transparencycolor), .4);
}
.passthrough-1c2ewQ.selected-2YhbGh {						/* rolesettings			permissions passthrough selected	*/
	background: rgb(var(--accentcolor));
}
.icon-3_8HGa {												/* rolesettings			everyone role icon					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.header-2mZ9Ov {											/* rolesettings			perms list header					*/
	background-color: transparent;
}
.titleElevated-c_kdi7,
.stickyHeaderElevated-I6QUOA {
	box-shadow: none;
}
.header-2mZ9Ov::after,
.header-2mZ9Ov::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.header-2mZ9Ov::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha)));
}
.header-2mZ9Ov::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
}
.roleDot-ZwSovK {											/* rolesettings			role dot							*/
	border: none;
}
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) {	/* rolesettings			role row							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) .circleButton-3RB01i {
	background-color: rgba(var(--transparencycolor), .2);
}
.roleRow-30TwGe:hover:not(.roleRowDisableHover-1HiqqT) .circleButton-3RB01i:hover {
	background-color: rgb(var(--accentcolor));
}
.roleRow-30TwGe:before,
.roleRow-30TwGe:last-child:after {
	background-color: var(--background-modifier-accent);
}
.memberRow-1wwtfV:hover {									/* rolesettings			member row							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm {		/* rolesettings			colorswatch nocolor					*/
	border-color: rgba(var(--textbrightest), .3);
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm .colorPickerDropperFg-3jYKWI {
	fill: var(--header-primary);
}
#app-mount .colorPickerSwatch-5GX3Ve.noColor-1pdBDm polyline {
	stroke: var(--header-primary);
}
.previewContainer-1KQDJS {									/* rolesettings			preview								*/
	border: none;
}
.messageContainer-1DiFnQ {									/* rolesettings			preview message						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.theme-light .messageContainer-1DiFnQ {
	display: none;
}
.addMemberRow-3-w-9X.selectedRow-1QP7qb {					/* rolesettings			add member row						*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .emojiAliasInput-1y-NBz .emojiInput-1aLNse {		/* emojisettings		nameinput							*/
	background-color: rgba(var(--transparencycolor), .1);
}

#app-mount .auditLog-3jNbM6 {								/* auditlogs			logitem								*/
	border-color: rgba(var(--transparencycolor), .1);
	color: var(--text-muted);
}
#app-mount .headerClickable-2IVFo9,							/* auditlogs			loginner							*/
#app-mount .headerDefault-1wrJcN {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-secondary);
}
#app-mount .headerExpanded-CUEwZ5 {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .divider-1pnAR2 {								/* auditlogs			loginnerdivider						*/
	background-color: var(--background-modifier-accent);
}
#app-mount .changeDetails-bk98pu {							/* auditlogs			logdetails							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .userHook-3AdCBF {								/* auditlogs			userhook							*/
	color: var(--header-primary);
}
#app-mount .auditLog-3jNbM6 strong {						/* auditlogs			targets								*/
	color: var(--header-primary);
}
#app-mount .timestamp-1mruiI {								/* auditlogs			timestamp							*/
	color: var(--text-muted);
}
#app-mount .expandForeground-1nZ4VR {						/* auditlogs			expandarrow							*/
	stroke: var(--header-secondary);
}
.themeOverrideLight-3bx_5B.icon-RTGJu3,						/* auditlogs			logicon								*/
.themeOverrideDark-1u5Vo0.icon-RTGJu3,
#app-mount .icon-RTGJu3 {
	background: none !important;
}
.icon-RTGJu3::before {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: var(--header-primary);
}
.icon-RTGJu3.targetAll-13V3n6::before {
	-webkit-mask: url(https://discord.com/assets/fc3f5f9be1a4db14b02336b7cb02e6ce.svg);
}
.icon-RTGJu3.targetBan-3mbIPL::before {
	-webkit-mask: url(https://discord.com/assets/edb23a53ea40ac60f212ebae66e5c5c7.svg);
}
.icon-RTGJu3.targetChannel-TrRFlx::before {
	-webkit-mask: url(https://discord.com/assets/343c9ff4c775c66a7d4af1f8691c34e0.svg);
}
.icon-RTGJu3.targetGuild-mDWfAV::before {
	-webkit-mask: url(https://discord.com/assets/30af96a386520760ad107c5b77ba002a.svg);
}
.icon-RTGJu3.targetEmoji-3vhPhM::before {
	-webkit-mask: url(https://discord.com/assets/7a9bf92329dad473ef0383ae75367215.svg);
}
.icon-RTGJu3.targetInvite-1RQBlr::before {
	-webkit-mask: url(https://discord.com/assets/4b33371531a1a89f99296a73fc9ef588.svg);
}
.icon-RTGJu3.targetMemberRole-jowY3I::before {
	-webkit-mask: url(https://discord.com/assets/a9098042cb36b955c5021259f1d48f91.svg);
}
.icon-RTGJu3.targetMember-2iuwxX::before {
	-webkit-mask: url(https://discord.com/assets/af043346e036ef7b1aac1cf42cd1e699.svg);
}
.icon-RTGJu3.targetPermission-ZRUN5n::before {
	-webkit-mask: url(https://discord.com/assets/2a37995eb832bae805190a93ba043857.svg);
}
.icon-RTGJu3.targetRole-2MoUny::before {
	-webkit-mask: url(https://discord.com/assets/0176a91b4c44ed05c05af68784e78da8.svg);
}
.icon-RTGJu3.targetVanityUrl-3OpsYX::before {
	-webkit-mask: url(https://discord.com/assets/84215a5fec3d9de9960a225143238d74.svg);
}
.icon-RTGJu3.targetWebhook-1xS7Z7::before {
	-webkit-mask: url(https://discord.com/assets/a6975850d800aa86162b4aa5f18c41ac.svg);
}
.icon-RTGJu3.targetWidget-3hFVSM::before {
	-webkit-mask: url(https://discord.com/assets/4ac0e382cc7b8aa0cb1d6d074b0e8ba5.svg);
}
.icon-RTGJu3.targetMessage-2kBYMT::before {
	-webkit-mask: url(https://discord.com/assets/8c85e30795486caa8caacd829703459d.svg);
}
.icon-RTGJu3.targetIntegration-3rnyMN::before {
	-webkit-mask: url(https://discord.com/assets/da8463a04b4a289801d2516f50eb4c19.svg);
}

#app-mount .card-o7rAq- {									/* integrationsettings	card								*/
	border-color: rgba(var(--transparencycolor), .1)
}
#app-mount .card-3IImnr {									/* integrationsettings	webhook card						*/
	border-color: rgba(var(--transparencycolor), .1)
}
#app-mount .card-1o0mns {									/* integrationsettings	apps card							*/
	border-color: rgba(var(--transparencycolor), .1)
}
#app-mount .card-11DMwv {									/* integrationsettings	follows card						*/
	border-color: rgba(var(--transparencycolor), .1)
}
.iconWrapper-lS1uig {										/* integrationsettings	icon								*/
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .footerImage-4UrEF0 {
    background-image: url(https://discord.com/assets/36d0e0bb009fa362c2533003c0af67b5.svg);
	opacity: 0.6;
}

.guildDetails-2p1NmK {										/* communitysettings	intro		details					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.featureCard-1RR4Tl {										/* communitysettings	intro		featurecard				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.featureIcon-3p1TC_ {										/* communitysettings	intro		featureicon				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.checklistContainer-mFJZEJ {								/* communitysettings	intro		checklist				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.checklistHeader-1KWcEY {									/* communitysettings	intro		checklist header		*/
	background-color: rgba(var(--transparencycolor), .3);
}

.upsellContainer-L9xv7w {									/* communitysettings	general		upsellcontainer			*/
	background-color: rgba(var(--transparencycolor), .2);
}
.upsellFooter-ZYsio_ {										/* communitysettings	general		upsellfooter			*/
	background-color: rgba(var(--transparencycolor), .2);
}

.developerPortalCtaWrapper-2XNafh {							/* communitysettings	analytics	info					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.analyticsCard-qckucw {										/* communitysettings	analytics	card					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.backgroundAccent-349kuI {									/* communitysettings	analytics	error					*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .card-3_CqkU {									/* communitysettings	discovery	card					*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .iconMask-30Tvqs {								/* communitysettings	discovery	icon					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.perkArt-1SGWbA {											/* communitysettings	discovery	perk					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.container-2w0lh0 {											/* communitysettings	discovery	checklist				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.header-2Y0-A- {											/* communitysettings	discovery	checklist header		*/
	background-color: rgba(var(--transparencycolor), .3);
}

.exampleContainer-3ekFIr,									/* communitysettings	rules		example					*/
.exampleContainer-25sB-A {									/* communitysettings	welcome		example					*/
	background: transparent;
	position: relative;
}
.exampleContainer-3ekFIr > *,
.exampleContainer-25sB-A > * {
	z-index: 1;
}
.exampleContainer-3ekFIr::after,
.exampleContainer-25sB-A::after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), .5);
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/discord_window_placeholder.svg) 0 0/cover no-repeat;
}
#app-mount .exampleModal-2oh58d,							/* communitysettings	rules		examplemodal			*/
#app-mount .exampleModal-2X2Vf8 {							/* communitysettings	welcome		examplemodal			*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	border-radius: 5px;
}
.exampleModal-2oh58d > *,
.exampleModal-2X2Vf8 > * {
	z-index: 1;
}
.exampleModal-2oh58d::before,
.exampleModal-2X2Vf8::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
}
.exampleModal-2oh58d::after,
.exampleModal-2X2Vf8::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
}

.guildSidebar-339BqP {										/* communitysettings	rules		example sidebar			*/
	background-color: rgba(var(--transparencycolor), .4);
	margin-right: 0 !important;
}
.content-BMIBeK {											/* communitysettings	rules		example inner			*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .footer-1JuRYY {									/* communitysettings	rules		example footer			*/
	background: transparent;
}
.exampleTextSingleLine-1kvErc {								/* communitysettings	rules		example line			*/
	background-color: rgba(var(--textbrightest), .3);
}

.enableContainer-2DIT9Q {									/* communitysettings	rules		enablecontainer			*/
	background-color: rgba(var(--transparencycolor), .3);
}
.icon-1CGepy {												/* communitysettings	rules		category icon			*/
	background-color: rgba(var(--transparencycolor), .2);
}
.settingsFormItem-103g1I {									/* communitysettings	rules		form					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.getStartedWrapper-2AGgRZ {									/* communitysettings	rules		getstarted				*/
	background-color: rgba(var(--transparencycolor), .2);
}
.exampleRule-32tIs5 {										/* communitysettings	rules		example rule			*/
	background-color: rgba(var(--transparencycolor), .4);
}
.rulesTextAreaInput-2aGfKB {								/* communitysettings	rules		edit rule				*/
	border-color: rgba(var(--transparencycolor), .3);
}
.rulesTextAreaInput-2aGfKB:hover:not(:focus) {
	border-color: rgb(var(--transparencycolor));
}
.editCircle-y9c7xP {										/* communitysettings	rules		editcirle				*/
	background-color: rgba(var(--transparencycolor), .4);
}
.editButton-1MavoF {										/* communitysettings	rules		editbutton				*/
	background-color: rgba(var(--transparencycolor), .4);
}
.editButton-1MavoF:hover {
	background-color: rgba(var(--transparencycolor), .6);
}
.formFieldWrapper-malor5,
.settingsFormFieldWrapper-3Y77Pr {							/* communitysettings	rules		form field				*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .2);
}

.editCircle-ityklj {										/* communitysettings	welcome		editcirle				*/
	background-color: rgba(var(--transparencycolor), .4);
}
.optionContainer-1FtykV {									/* communitysettings	welcome		exampleoption			*/
	background-color: rgba(var(--transparencycolor), .3);
}
.enableContainer-6E-puu {									/* communitysettings	welcome		previewheader			*/
	background-color: rgba(var(--transparencycolor), .4);
}
.previewContainer-1SS3uO {									/* communitysettings	welcome		previewcontainer		*/
	background-color: rgba(var(--transparencycolor), .2);
}
.welcomeChannel-1rFrIO {									/* communitysettings	welcome		welcomechannel			*/
	background-color: rgba(var(--transparencycolor), .4);
}
.channelIcon-1eKmlw {										/* communitysettings	welcome		channelicon			s	*/
	background-color: rgba(var(--transparencycolor), .4);
}

.descriptionBox-1EKQKL {									/* templatesettings		descriptionbox						*/
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .tierHeaderLocked-1a2opw {						/* boostsettings		tierheaderlocked					*/
	background-color: rgba(var(--transparencycolor), .4);
	color: var(--header-secondary);
}
#app-mount .tierHeaderUnlocked-2RhWqn {						/* boostsettings		tierheaderunlocked					*/
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .tierBody-x9kBBp {								/* boostsettings		tierbody							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .tierInProgress-3mBoXq {							/* boostsettings		tiermilestone						*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .background-3xPPFc {								/* boostsettings		tierbar	(settings)					*/
	color: rgba(var(--transparencycolor), .3);
}

#app-mount .member-1q7VfX {									/* membersettings		membercard							*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
#app-mount .member-1q7VfX .name-8yzEIY {					/* membersettings		membercardname						*/
	color: var(--header-primary);
}
#app-mount .member-1q7VfX .tag-1YGWN9 {						/* membersettings		membercardtag						*/
	color: var(--text-muted);
}
#app-mount .member-1q7VfX .roleWrapper-1Hde_V {				/* membersettings		rolewrapper							*/
	color: rgba(var(--textbrightest),.8);
}
#app-mount .actionButton-VzECiy {							/* membersettings		addrolebutton						*/
	border-color: var(--header-secondary);
	color: var(--header-secondary);
}
#app-mount .member-1q7VfX .overflowIconFg-QMRRFI {			/* membersettings		3-dot icon							*/
	fill: var(--header-primary);
}
#app-mount .member-1q7VfX .ownerHelpIcon-3ItaBx {			/* membersettings		help icon							*/
	color: var(--header-primary);
}

#app-mount .overflowRolesPopout-140n9i,						/* membersettings		roleoverflow popout					*/
#app-mount .overflowRolesPopoutArrow-2O66oH {
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .2), 0 2px 10px 0 rgba(var(--transparencycolor), .2);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.overflowRolesPopout-140n9i::before,
.overflowRolesPopoutArrow-2O66oH::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.overflowRolesPopout-140n9i::after,
.overflowRolesPopoutArrow-2O66oH::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.overflowRolesPopoutHeaderIcon-6PNEZA path {
	fill: var(--header-secondary);
}
.overflowRolesPopoutHeaderText-1SW-y3 {
	color: var(--header-secondary);
}

#app-mount .inviteSettingsInviteRow-3p2O-N {				/* invitesettings		invitecard							*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}

#app-mount .bannedUser-1IalTM {								/* bansettings			bancard								*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
#app-mount .bannedUser-1IalTM .username-1b3MVI {			/* invitesettings		username							*/
	color: var(--header-primary);
}
#app-mount .bannedUserModal-3RJCOV .reasonHeader-2etdjy {	/* invitesettings		banmodalreasonheader				*/
	color: var(--text-normal);
}
#app-mount .bannedUser-1IalTM .username-1b3MVI .discrim-oGb-FO,
#app-mount .bannedUserModal-3RJCOV .reason-YbfGC6,			/* invitesettings		banmodalreason						*/
#app-mount .bannedUserModal-3RJCOV .userDiscrim-1D2NlF {	/* invitesettings		discriminator						*/
	color: var(--text-muted);
}


/* ~~~~		13.		MODALS							~~~~ */

.layer-2KE1M9:nth-child(1),
.withLayer-RoELSG:nth-child(1) {
	z-index: 1002;
}
.layer-2KE1M9:nth-child(2),
.withLayer-RoELSG:nth-child(2) {
	z-index: 1003;
}
.layer-2KE1M9:nth-child(3),
.withLayer-RoELSG:nth-child(3) {
	z-index: 1004;
}
.layer-2KE1M9:nth-child(4),
.withLayer-RoELSG:nth-child(4) {
	z-index: 1005;
}
.layer-2KE1M9:nth-child(5),
.withLayer-RoELSG:nth-child(5) {
	z-index: 1006;
}
.layer-2KE1M9:nth-child(6),
.withLayer-RoELSG:nth-child(6) {
	z-index: 1007;
}
.layer-2KE1M9:nth-child(7),
.withLayer-RoELSG:nth-child(7) {
	z-index: 1008;
}
.layer-2KE1M9:nth-child(8),
.withLayer-RoELSG:nth-child(8) {
	z-index: 1009;
}
.layer-2KE1M9:nth-child(9),
.withLayer-RoELSG:nth-child(9) {
	z-index: 1010;
}

#app-mount .root-1gCeng,									/* modal				container (foldersettings)			*/
#app-mount .modal-yWgWj- {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	border-radius: 5px;
}
.root-1gCeng > *,
.modal-yWgWj- > * {
	z-index: 1;
}
.root-1gCeng::before,
.modal-yWgWj-::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.root-1gCeng::after,
.modal-yWgWj-::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.root-1gCeng .modal-yWgWj-::before,
.modal-qgFCbT::before,
.root-1gCeng .modal-yWgWj-::after,
.modal-qgFCbT::after {
	display: none;
}
.header-1TKi98 > .wrapper-1sSZUt {
	flex: 1 0 auto;
}
#app-mount .separator-2-RRj_ {
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor),.3), 0 1px 2px 0 rgba(var(--transparencycolor),.3);
}
#app-mount .modalTextContainer-ITvzbi {						/* modal				text file						*/
	background-color: rgba(var(--transparencycolor), .5);
	border: none;
}
#app-mount .footer-2gL1pp {									/* modal				footer							*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
	z-index: 0;
}
#app-mount .footer-1lnhms {									/* modal				footer info						*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .close-hZ94c6 {									/* modal				closebutton						*/
	z-index: 2;
}

.tabBarContainer-37hZsr {									/* modal				tabbarcontainer					*/
	border-top-color: rgba(var(--transparencycolor), .3);
}
#app-mount .modal-6GHvdM .tabBarContainer-37hZsr {
	background: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .1);
}

#app-mount .separator-19P9q2 {
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor),.3), 0 1px 2px 0 rgba(var(--transparencycolor),.3);
}
#app-mount .divider-3WKGWk {
	border-color: var(--background-modifier-accent);
}

#app-mount .subHeader-3TFIST {
	color: var(--header-secondary);
}
#app-mount .sectionBody-DUrZPU,
#app-mount .subHeader-3FXnUc {
	color: var(--header-secondary);
}

#app-mount .message-1F58Gs {
	color: var(--header-secondary);
}
#app-mount .secondaryButton-197mr8 {
	color: var(--header-primary);
}
#app-mount .imageUpgrade-moI_hv {
	background-image: url(https://discord.com/assets/81ded87ebac6f9d55e8624a3e5167c8f.svg);
}
#app-mount .imageCancel-2x4k_k {
	background: url(https://discord.com/assets/03863b539aec443327ca2ffc51a89dac.svg);
}
#app-mount .imageUnclaimed-5nJyYs {
	background-image: url(https://discord.com/assets/3b65c741e596bc0979f7ba0c42de6fff.svg);
	opacity: .5;
}
#app-mount .imageUnverified-2NLnW6 {
	background-image: url(https://discord.com/assets/e260177e5165e6789e30b9592df75424.svg);
	opacity: .5;
}

#app-mount .divider-1que2t {
	border-color: var(--background-modifier-accent);
}
#app-mount .backButtonColor-N09dXJ {
	color: var(--header-primary);
}
#app-mount .checkboxLabel-3WoD3k {
	color: var(--header-secondary);
}

/* ----		13.1.	USERMODAL						----- */

#app-mount .root-3QyAh1 {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.root-3QyAh1::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	filter: blur(var(--popoutblur));
	background-attachment: fixed;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.root-3QyAh1::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .root-3QyAh1 .topSection-y3p-_D {				/* modal				topsection							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.root-3QyAh1 .avatar-AvHqJA {								/* modal				avatar								*/
	background: transparent;
	border-color: transparent;
	z-index: 1;
}
.root-3QyAh1 .avatar-AvHqJA::before,
.root-3QyAh1 .avatar-AvHqJA::after {
	content: "";
	position: absolute;
	top: -8px;
	right: -8px;
	bottom: -8px;
	left: -8px;
	border-radius: 50%;
	pointer-events: none;
	z-index: -1;
}
.root-3QyAh1 .avatar-AvHqJA::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	filter: blur(var(--popoutblur));
	background-attachment: fixed;
}
.root-3QyAh1 .avatar-AvHqJA::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + .375));
}
#app-mount .body-r6_QPy {									/* modal				body								*/
	background-color: transparent;
}
.listRow-1iDGel:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.emptyIcon-1yiM-z {											/* body					emptypic							*/
	opacity: .5;
}

/* ----		13.2.	GUILDADD/CREATION				----- */

.container-UC8Ug1 {											/* modal				item								*/
	background-color: rgb(var(--transparencycolor), .2);
	border: none;
}
.container-UC8Ug1:hover {
	background-color: rgb(var(--transparencycolor), .4);
}
.text-1FOLJS {												/* modal				text								*/
	color: var(--header-secondary);
}
.container-UC8Ug1:hover .text-1FOLJS {
	color: var(--header-primary);
}
.arrow-hynWUl {												/* modal				arrow								*/
	object-position: -999999px -999999px;
	-webkit-mask: url(https://discord.com/assets/69a0ea5dbf79a129c81a0cb171b60b7a.svg) center/cover no-repeat;
	background: var(--header-secondary);
}
.container-UC8Ug1:hover .arrow-hynWUl {
	background: var(--header-primary);
}
.input--jS-j2 {												/* modal				invite input						*/
	background: transparent;
}
.inputInner-2akrSS {										/* modal				invite input inner					*/
	border: 1px solid var(--deprecated-text-input-border);
}

/* ----		13.3.	REGIONSELECTMODAL				---- */

#app-mount .regionSelectModal-12e-57 {						/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.regionSelectModal-12e-57::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.regionSelectModal-12e-57::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3 {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3:hover {
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .regionSelect-3lf4eE.regionSelectLoading-34I21m {
	border: 1px solid var(--header-secondary);
}
#app-mount .regionSelect-3lf4eE button {
	border: 1px solid var(--header-secondary);
}
#app-mount .regionSelect-3lf4eE .regionSelectInner-24f4Ce {
	border: 1px solid var(--header-secondary);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalFooter-20C5iA {
	color: var(--text-muted);
}
#app-mount .regionSelectName-2-2FWh {
	color: var(--text-muted);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3:hover .regionSelectName-2-2FWh {
	color: var(--text-normal);
}
#app-mount .regionSelect-3lf4eE:hover button {
	color: var(--header-primary);
}
#app-mount .container-1s4HBn.hover-2AGf5p {
	border-color: var(--deprecated-text-input-border-hover);
}
#app-mount .flag-16iIBd.vip-3pFIN8::after {
	border-color: rgba(var(--transparencycolor), .5);
}

/* ----		13.4.	UPLOADMODAL						---- */

#app-mount .uploadModal-2ifh8j {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	border-radius: 10px;
}
.uploadModal-2ifh8j::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 10px;
	z-index: -1;
}
.uploadModal-2ifh8j::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 10px;
	z-index: -1;
}

.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc {
	width: unset;
}
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo .title-2Vtl4y,
.uploadModalIn-1z07Bv .uploadDropModal-2kTwbc .inner-3nWsbo .instructions-2Du9gG {
	text-shadow: 1px 1px var(--textshadow);
}
.uploadModal-2ifh8j .inner-zqa7da {							/* modal				channeltextarea						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.uploadModal-2ifh8j .footer-3mqk7D {						/* modal				footer								*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
}
.uploadModal-2ifh8j .inner-3nWsbo .file-34mY5K .icon-kyxXVr.image-2yrs5j {
	box-shadow: 0 2px 8px rgba(var(--transparencycolor), .4);
}

/* ----		13.5.	KEYBOARDSHORTCUTSMODAL			---- */

#app-mount .keyboardShortcutsModal-3piNz7 {					/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.keyboardShortcutsModal-3piNz7::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.keyboardShortcutsModal-3piNz7::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .modalTitle-37O4n6 {								/* modal				title								*/
	color: var(--header-primary);
}
#app-mount .modalSubtitle-1Pj5nv {							/* modal				subtitle							*/
	border-color: var(--background-modifier-accent);
	color: var(--text-normal);
}
#app-mount .keyboardShortcutList-13cQ-8 .keybindGroup--6Qp-w .keybindDescription-2RDbC2 {
	color: var(--header-secondary);
}
#app-mount .keybindShortcut-1BD6Z1 {
	color: var(--header-primary);
}
#app-mount .keybindShortcut-1BD6Z1 span {
	background-color: var(--text-muted);
	border: 1px solid rgba(0, 0, 0, .4);
	box-shadow: inset 0 -4px 0 rgba(0, 0, 0, .4);
	color: var(--header-primary);
}
#app-mount .keybindShortcut-1BD6Z1 span:active {
	box-shadow: inset 0 -2px 0 rgba(0, 0, 0, .6);
	border: 1px solid rgb(0, 0, 0);
	color: var(--header-secondary);
}
#app-mount .keybindShortcut-1BD6Z1 span .bindArrow-2X3Aom g {
	fill: var(--header-primary);
}
#app-mount .keybindShortcut-1BD6Z1 span:active .bindArrow-2X3Aom g {
	fill: var(--header-secondary);
}
#app-mount .keybindShortcutTipsSelect-HDyfe8:last-of-type::before {
	background-color: var(--interactive-muted);
}
#app-mount .tabButton-1n4gNP {
	background-color: var(--text-muted);
	border: 1px solid rgb(0, 0, 0, .4);
	border-radius: 4px;
	box-shadow: inset 0 -4px 0 rgb(0, 0, 0, .4);
	color: var(--header-primary);
}
#app-mount .tabButton-1n4gNP rect[fill="#4F545C"],
#app-mount .tabButton-1n4gNP path[fill="#36393F"] {
	display: none;
}

/* ----		13.6.	QUICKSWITCHER					---- */

#app-mount .quickswitcher-3JagVE {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.quickswitcher-3JagVE::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.quickswitcher-3JagVE::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.scroller-zPkAnE {
	background-color: transparent;
}
#app-mount .input-2VB9rf {									/* modal				input								*/
	background-color: rgba(var(--transparencycolor), .4);
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .resultFocused-3aIoYe {							/* modal				resultfocused						*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		13.7.	INVITEMODAL/GROUPCREATE			---- */

#app-mount .contentWrapper-3WC1ID {								/* modal				guildinvitemodal				*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.contentWrapper-3WC1ID::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-3WC1ID::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .friendSelected-1sa4bG,								/* modal				groupdmrow						*/
#app-mount .inviteRow-2L02ae:hover {							/* modal				guildrow						*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .friend-3KALPe,										/* modal				groupdmrow						*/
#app-mount .inviteRowName-1tVaxu {								/* modal				username						*/
	color: var(--header-secondary);
}
#app-mount .friendSelected-1sa4bG,
#app-mount .inviteRow-2L02ae:hover .inviteRowName-1tVaxu {
	color: var(--header-primary);
}
#app-mount .checkBoxLabel-4PWfpk,
#app-mount .footerText-2a7NxZ,
#app-mount .subTitle-3TUjmF,
#app-mount .subtitle-2P4u9v,
#app-mount .subText-bCySlS {
	color: var(--header-secondary);
}
.tag-2gHSR7 {													/* modal				added user						*/
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
.pill-1dHPfk {
	background-color: rgba(var(--transparencycolor), .5);
}

/* ----		13.8.	LOGINSCREEN						---- */

#app-mount .wrapper-3Q5DdO {								/* login				wrapper								*/
	background: transparent;
}
.wrapper-3Q5DdO::before,									/* login				winbuttonshadow						*/
.wrapper-3Q5DdO .rightSplit-2US0xy,							/* login				background							*/
.wrapper-3Q5DdO .canvas-3XuBXe {							/* login				movingshadow						*/
	display: none;
}
.theme-dark.authBox-hW6HRx,									/* login				modal								*/
.theme-light.authBox-hW6HRx {
	background-color: rgba(var(--transparencycolor), .5);
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--text-muted);
	position: relative;
	overflow: hidden;
}

/* ----		13.9.	TERMACCEPTMODAL					---- */

#app-mount .modal-DRZfgq {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.modal-DRZfgq::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.modal-DRZfgq::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

[style*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"],	/* modal				image								*/
[src*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"] {
	filter: brightness(85%) invert(100%);
	opacity: 0.7;
}

#app-mount .ack-2yIUvY {									/* modal				acklabel							*/
	color: var(--header-secondary);
}
#app-mount .buttonContainer-3S_miP {						/* modal				footer								*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
}

/* ----		13.10.	DOWNLOADAPPMODAL				---- */

#app-mount .downloadApps-wbBFdZ {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.downloadApps-wbBFdZ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.downloadApps-wbBFdZ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.downloadApps-wbBFdZ .header-nJMe-Q {
	color: var(--text-normal);
}
.downloadApps-wbBFdZ .footer-1nkeBm {
	color: var(--text-muted);
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 {
	border-color: var(--header-secondary);
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 p {
	color: var(--header-secondary);
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236 .downloadButton-1bWXpg {
	background-color: var(--header-secondary);
}
.downloadApps-wbBFdZ .platforms-28Rb-3 .platform-iik236.active-iLSdWQ .downloadButton-1bWXpg {
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		13.11.	GUILDBOOSTMODAL					---- */

#app-mount .perksModal-fSYqOq {								/* modal				wrapper								*/
	background-color: transparent;
}
.carouselContainer-2-vIZS {									/* modal				scrollercontainer					*/
	-webkit-mask: linear-gradient(to right, rgba(0,0,0,0) 0px, rgba(0,0,0,1) 60px, rgba(0,0,0,1) calc(100vw - 60px), rgba(0,0,0,0) 100vw);
}
.carouselGradientEdge-2W94ou {								/* modal				scrollergradient					*/
	display: none;
}
#app-mount .subscriberCount-27QHc5 {						/* modal				subcount							*/
	color: var(--header-secondary);
}
#app-mount .subscriberCount-27QHc5 strong {
	color: var(--text-normal);
}
#app-mount .moreSubscribers-1cuWDE {						/* modal				suboverflow							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-primary)
}

#app-mount .subscribersPopout-2CP6Ln {						/* subpopout			container							*/
	background-color: transparent;
	box-shadow: 0 2px 10px rgba(var(--transparencycolor), .2);
	overflow: hidden;
}
.subscribersPopout-2CP6Ln::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.subscribersPopout-2CP6Ln::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.35));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .subscribersPopoutUser-3rC75S {					/* subpopout			users								*/
	color: var(--header-secondary);
}

#app-mount .ctaBar-2UsjF2 {									/* current boost stats	container							*/
	position: relative;
	background-color: rgba(var(--transparencycolor), .4);
	background-image: none;
}
#app-mount .ctaBar-2UsjF2::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background-color: rgb(var(--accentcolor));
	-webkit-mask: url(https://discord.com/assets/94ff6fdc535b6ecb7b1bc54f2dd56a10.svg);
}
.guildIcon-3raYf3 {											/* current boost stats	guild icon							*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .perk-2WeBWW {									/* modal				perkcard							*/
	background-color: rgba(var(--transparencycolor), .4);
}

#app-mount .headerLogo--hLLAk {
	color: var(--header-primary);
}
#app-mount .tierHeaderLocked-1s2JJz {						/* modal				tierheaderlocked 					*/
	background-color: rgba(var(--transparencycolor), .4);
	color: var(--text-muted);
}
#app-mount .tierLock-3CSxSX {								/* modal				tierlock 							*/
	color: var(--interactive-muted);
}
#app-mount .tierHeaderUnlocked-1n-OTI {						/* modal				tierheaderunlocked 					*/
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .tierBody-16Chc9 {								/* modal				tierbody 							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .tierMarkerBackground-3q29am {					/* modal				tiermilestone 						*/
	background: transparent;
}
#app-mount .tierMarkerInProgress-24LMzJ {
	background: rgba(var(--transparencycolor), .3) !important;
}
#app-mount .selectedTier-1JkO7i .tierMarker-5HkGJ_ {
	box-shadow: 0 4px 8px rgba(var(--transparencycolor), .24);
}
#app-mount .tierMarkerLabelText-F_zS1F:not(.isAccomplished-2EpZfL):hover {
	background: rgba(var(--transparencycolor), .3);
}
#app-mount .barBackground-2EEiLw {							/* modal				tierbar 								*/
	background: linear-gradient(to right, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 3%, rgba(var(--transparencycolor), .3) 3%, rgba(var(--transparencycolor), .3) 30.2%, rgba(0,0,0,0) 30.2%, rgba(0,0,0,0) 36.2%, rgba(var(--transparencycolor), .3) 36.2%, rgba(var(--transparencycolor), .3) 63.5%, rgba(0,0,0,0) 63.5%, rgba(0,0,0,0) 69.5%, rgba(var(--transparencycolor), .3) 69.5%, rgba(var(--transparencycolor), .3) 96.7%, rgba(0,0,0,0) 96.7%, rgba(0,0,0,0) 100%);
}
.barSecondary-3B1aP2 {
	background-color: rgb(var(--accentcolor));
}
.wrapper-3nSjSv .heading-4znNKq {							/* modal				boostaddwrapper header						*/
	text-shadow: 1px 1px var(--textshadow);
}
.tier-1EY-yj {												/* modal				boostaddwrapper tier						*/
	background-color: rgb(var(--transparencycolor), .3);
}
#app-mount .giftIcon-ZxlWk5 {								/* modal				gifticon							*/
	color: var(--header-secondary);
	margin: 0 18px;
}
#app-mount .button-38aScr .giftIcon-ZxlWk5 {
	color: currentColor;
}
#app-mount .badgeIconWithoutSubscribers-3A9Xol {
	color: var(--text-muted);
}
#app-mount .tierPill-1yRO48 {
	background: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .tierPillStar-34rvoJ {
	color: var(--header-primary);
}
#app-mount .tierPillGem-3zcO2T {
	color: var(--interactive-muted);
}
#app-mount .tierPill-3gJ0eN {
	background: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .perk-2WeBWW {
	background: rgba(var(--transparencycolor), .2);
}

.header-1F6gxU {											/* prebuy popout		header								*/
	background: rgba(var(--transparencycolor), .3);
	padding-bottom: 10px;
	margin-bottom: 10px;
}
#app-mount .iconWrapper-3LVgIo {							/* prebuy popout		amount icon wrapper					*/
	background: rgba(var(--transparencycolor), .3);
}
.icon-TYbVk4:hover {										/* prebuy popout		amount icon							*/
	background: rgb(var(--accentcolor));
}
.upsellFooter-6EgwMe {										/* prebuy popout		footer details						*/
	background: rgba(var(--transparencycolor), .3);
}
.perksList-1vtwXn {											/* prebuy popout		perkslist							*/
	background: rgba(var(--transparencycolor), .3);
}

#app-mount .selectGuild-1Ygl76:hover {
	background-color: rgba(var(--transparencycolor), .3);
}

/* ----		13.12.	REACTIONSMODAL					---- */

#app-mount .scroller-1-nKid {								/* modal				sidebar								*/
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .reactors-Blmlhw {								/* modal				list								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .reactionDefault-GBA58K:hover {					/* modal				reaction							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .reactionSelected-1pqISm {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .remove-3V-yj8 {									/* modal				remove								*/
	color: var(--interactive-normal);
}
#app-mount .remove-3V-yj8:hover {
	background-color: rgba(var(--transparencycolor), .4);
	color: var(--interactive-hover);
}
#app-mount .discriminator-byOsvi {							/* modal				discriminator						*/
	color: var(--text-muted);
}

/* ----		13.13.	GUILDTEMPLATEMODAL				---- */

.ctaSection-izWwhs {										/* modal				ctasection							*/
	background-color: transparent;
}
.formSection-1NFAGI {										/* modal				formsection							*/
	background-color: transparent;
}

.usagePill-2WGS4A {											/* modal				usagepill 1							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.usagePill-_nSrnP {											/* modal				usagePill 2							*/
	background-color: rgba(var(--transparencycolor), .3);
}

.channelsWrapper-2HhUER {									/* modal				channelswrapper						*/
	background-color: rgba(var(--transparencycolor), .3);
}

.rolesWrapper-2yOx9S {										/* modal				roleswrapper							*/
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .role-3paDXR {									/* modal				role								*/
	border-color: rgba(var(--textbrighter), .6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-3paDXR[style*="border-color: rgba(185, 187, 190, .6)"] {
	border-color: rgba(var(--textbrighter), .6) !important;
}
#app-mount .role-3paDXR .roleName-1JcOmP {					/* modal				rolename							*/
	color: rgb(var(--textbrightest));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-3paDXR .roleCircle-3DE8xJ {				/* modal				rolecircle							*/
	position: absolute;
	background-color: rgb(var(--textbrighter));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	left: 0;
	top: 0;
}
#app-mount .role-3paDXR .roleCircle-3DE8xJ[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--textbrighter)) !important;
}

/* ----		13.14.	GUILDWELCOMEMODAL				---- */

.optionContainer-15srkc {									/* modal				option								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.optionContainer-15srkc:hover {
	background-color: rgba(var(--transparencycolor), .4);
}

/* ----		13.15.	GUILDRULESMODAL					---- */

.guildSidebar-2OCzWB {										/* modal				sidebar								*/
	background-color: rgba(var(--transparencycolor), .4);
}
.modal-f02hVt {												/* modal				inner								*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		13.16.	GUILDFEEDBACKMODAL				---- */

.root-2IyrUe {												/* modal				items								*/
	background-color: transparent;
	border-radius: 0;
}
.option-3Ztn6N {											/* modal				item								*/
	background-color: rgb(var(--transparencycolor), .2);
	border: none;
	border-radius: 8px;
	margin-bottom: 8px;
}
.option-3Ztn6N:hover {
	background-color: rgb(var(--transparencycolor), .4);
}

/* ----		13.17.	SCREENSHAREMODAL				---- */

#app-mount .sourceThumbnail-27dolk {						/* modal				preview tiles						*/
	background-color: rgba(var(--transparencycolor), .4);
	box-shadow: 0 2px 5px rgba(var(--transparencycolor), .2), 0 0 0 1px rgba(var(--transparencycolor), .6);
}
.card-2Mz_4z {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .4);
}
#app-mount .item-3T2z1R {
	border-color: rgba(var(--transparencycolor), .4);
}
.selectorButton-EEUWed:not(.selectorButtonSelected-t5V9On) {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .userListOverflow-cTtEue {
	background: rgba(var(--transparencycolor), .5);
}

/* ----		13.18.	PHONEVERIFICATIONMODAL			---- */

.phoneField-38N1bJ {
	background-color: rgba(var(--transparencycolor), .2);
}
.phoneField-38N1bJ .inputField-aNPXsv {
	background-color: transparent;
}
.phoneFieldPopout-7PzjOO {
	position: absolute !important;
}

/* ----		13.19.	NOTIFICATIONSMODAL				---- */

#app-mount .channelName-28iMRJ {
	color: var(--header-primary);
}
#app-mount .guildName-3WI6ml,
#app-mount .override-2YgiXd,
#app-mount .overrideHighlight-YPcBxt {
	color: var(--header-secondary);
}
#app-mount .override-2YgiXd:hover {
	background-color: rgba(var(--backgroundtertiary),.1);
}
#app-mount .overrideHighlight-YPcBxt,
#app-mount .overrideHighlight-YPcBxt:hover {
	background-color: rgba(var(--backgroundtertiary),.3);
}
#app-mount .checkboxContainer-2vV9zd::before {
	background-color: rgba(var(--backgroundtertiary),.6);
}
#app-mount .overridePlaceholder-14_rPI {
	border: 1px dashed var(--background-floating);
}

/* ----		13.20.	DISCOVERYENTRYMODAL				---- */

.checkboxWrapper-SkhIWG.row-3QHy4I {
	background-color: rgba(var(--transparencycolor),.2);
}
.checkboxWrapper-SkhIWG.row-3QHy4I:hover:not(.checked-3_4uQ9) {
	background-color: rgba(var(--transparencycolor),.4);
}
.checkboxWrapper-SkhIWG.row-3QHy4I.checked-3_4uQ9 {
	background-color: rgb(var(--accentcolor));
}
.checkboxWrapper-SkhIWG.row-3QHy4I.checked-3_4uQ9 .colorStandard-2KCXvj {
	color: var(--header-primary);
}


/* ~~~~		14.		POPOUTS							~~~~ */

.layer-v9HyYc:nth-child(1) {
	z-index: 1002;
}
.layer-v9HyYc:nth-child(2) {
	z-index: 1003;
}
.layer-v9HyYc:nth-child(3) {
	z-index: 1004;
}
.layer-v9HyYc:nth-child(4) {
	z-index: 1005;
}
.layer-v9HyYc:nth-child(5) {
	z-index: 1006;
}
.layer-v9HyYc:nth-child(6) {
	z-index: 1007;
}
.layer-v9HyYc:nth-child(7) {
	z-index: 1008;
}
.layer-v9HyYc:nth-child(8) {
	z-index: 1009;
}
.layer-v9HyYc:nth-child(9) {
	z-index: 1010;
}

#app-mount .popout-2iWAc-:not(.noShadow-3pu20z) {
	box-shadow: 0 0 1px rgba(var(--transparencycolor), .2), 0 1px 4px rgba(var(--transparencycolor), .1);
}

#app-mount .themedPopout-1TrfdI {							/* themed popout		(for example mentionpopout)			*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
	position: relative;
}
.themedPopout-1TrfdI::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
.themedPopout-1TrfdI::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}

.selected-2114Fj,											/* popout				combobox selected					*/
.selected-2114Fj:hover {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .divider-1que2t {								/* popout				divider								*/
	border-color: var(--background-modifier-accent);
}

/* ----		14.1.	CONTEXTMENU						---- */

.styleFlexible-wGDiIL,										/* contextmenu			flexible							*/
.styleFixed-sX-yHV,											/* contextmenu			fixed								*/
.submenu-2-ysNh {											/* contextmenu			submenu								*/
	background: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
.styleFlexible-wGDiIL::before,
.styleFixed-sX-yHV::before,
.submenu-2-ysNh::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.styleFlexible-wGDiIL::after,
.styleFixed-sX-yHV::after,
.submenu-2-ysNh::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.3));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.submenu-2-ysNh {
	position: relative;
}
.container-1S6Mlq {											/* contextmenu			searchbar							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.item-1tOPte.colorDefault-2K3EoJ.focused-3afm-j,
.item-1tOPte.colorDefault-2K3EoJ:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(var(--transparencycolor), .2) !important;
}
.item-1tOPte.colorDanger-2qLCe1.focused-3afm-j,
.item-1tOPte.colorDanger-2qLCe1:hover:not(.hideInteraction-1iHO1O) {
	background-color: rgba(var(--dangercolor), .2) !important;
}
.item-1tOPte.colorBrand-ROmMP1.focused-3afm-j,
.item-1tOPte.colorBrand-ROmMP1:hover:not(.hideInteraction-1iHO1O),
.item-1tOPte.colorPremium-p4p7qO.focused-3afm-j,
.item-1tOPte.colorPremium-p4p7qO:hover:not(.hideInteraction-1iHO1O),
.item-1tOPte.colorDefault-2K3EoJ.focused-3afm-j[id="user-settings-cog-Discord_Nitro"],
.item-1tOPte.colorDefault-2K3EoJ:hover:not(.hideInteraction-1iHO1O)[id="user-settings-cog-Discord_Nitro"],
.item-1tOPte.colorDefault-2K3EoJ.focused-3afm-j[id="user-settings-cog-Nitro_Server_Boost"],
.item-1tOPte.colorDefault-2K3EoJ:hover:not(.hideInteraction-1iHO1O)[id="user-settings-cog-Nitro_Server_Boost"],
.item-1tOPte.colorDefault-2K3EoJ.focused-3afm-j[id="guild-context-guild-settings--GUILD_PREMIUM"],
.item-1tOPte.colorDefault-2K3EoJ:hover:not(.hideInteraction-1iHO1O)[id="guild-context-guild-settings--GUILD_PREMIUM"] {
	background-color: rgba(var(--accentcolor), .2) !important;
}
#app-mount .item-1tOPte .checkbox-3s5GYZ {					/* contextmenu			checkbox 							*/
	color: rgb(var(--accentcolor));
}
#app-mount .item-1tOPte.colorDanger-2qLCe1 .checkbox-3s5GYZ {
	color: rgb(var(--dangercolor));
}
#app-mount .item-1tOPte .check-1JyqgN {						/* contextmenu			checkmark 							*/
	color: #fff;
	stroke: var(--textshadow);
}
.button-F9qN4n {											/* contextmenu			quick reaction button				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.button-F9qN4n:hover {
	background-color: rgb(var(--accentcolor));
}

/* ----		14.2.	USERPOPOUT						---- */

.userPopout-xaxa6l {										/* popout				container							*/
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
.userPopout-xaxa6l::before,
.userPopout-xaxa6l::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	border-radius: 5px;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.userPopout-xaxa6l::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	filter: blur(var(--popoutblur));
	background-attachment: fixed;
}
.userPopout-xaxa6l::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
}
.headerNormal-1mX3KY {										/* popout				headernormal						*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .headerTop-2cWpdB,								/* popout				header inner						*/
#app-mount .activity-fViXj7 {								/* popout				activity							*/
	background: transparent;
	border: transparent;
}
.userPopout-xaxa6l .avatar-37jOim {							/* popout				avatar								*/
	background: transparent;
	border-color: transparent;
}
.userPopout-xaxa6l .avatar-37jOim::before,
.userPopout-xaxa6l .avatar-37jOim::after {
	content: "";
	position: absolute;
	top: -6px;
	right: -6px;
	bottom: -6px;
	left: -6px;
	border-radius: 50%;
	pointer-events: none;
	z-index: -1;
}
.userPopout-xaxa6l .avatar-37jOim::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	filter: blur(var(--popoutblur));
	background-attachment: fixed;
}
.userPopout-xaxa6l .avatar-37jOim::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + .375));
}
.aboutMeSection---MkQa {									/* popout				about me section					*/
	background-color: transparent;
}
.activity-3v9l4T {											/* popout				activity							*/
	padding: 0 16px 16px;
}

#app-mount .body-3HBlXn,									/* popout				body								*/
#app-mount .footer-1N3bR3 {									/* popout				footer								*/
	background-color: transparent;
	color: var(--header-secondary);
}
#app-mount .footer-1N3bR3 {
	border-color: var(--background-modifier-accent);
}

.root-3-B5F3 {												/* body					roles								*/
	max-height: 100px;
	overflow-x: hidden;
	overflow-y: scroll;
}
#app-mount .root-3-B5F3::-webkit-scrollbar {
	width: 4px;
}
#app-mount .role-2irmRk {									/* body					role								*/
	border-color: rgba(var(--textbrighter), .6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-2irmRk[style*="border-color: rgba(185, 187, 190, .6)"] {
	border-color: rgba(var(--textbrighter), .6) !important;
}
#app-mount .role-2irmRk .roleName-32vpEy {					/* body					rolename							*/
	color: rgb(var(--textbrightest));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j {				/* body					rolecircle							*/
	position: absolute;
	background-color: rgb(var(--textbrighter));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	left: 0;
	top: 0;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--textbrighter)) !important;
}
#app-mount .role-2irmRk .roleCircle-3xAZ1j:not(:empty):hover {
	opacity: 1;
	z-index: 2000;
	cursor: pointer;
}

.textarea-2r0oV8:focus {									/* body					note 								*/
	background-color: rgba(var(--transparencycolor), .2);
}

.wumpusWrapper-2-V9io {										/* footer				wumpus new user 					*/
	margin-top: 27px;
}
#app-mount .wumpusTooltip-mj7eo0 {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .wumpusTooltip-mj7eo0::after {
	border-color: transparent rgb(var(--accentcolor)) transparent transparent;
}

/* ----		14.3.	EMOJIPICKER						---- */

.contentWrapper-SvZHNd,										/* picker				expression wrapper					*/
.emojiPicker-3PwZFl,										/* picker				inner								*/
.diversitySelectorOptions-4YM-vX {							/* picker				diversityselector					*/
	background: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	overflow: hidden;
}
.contentWrapper-SvZHNd::before,
.emojiPicker-3PwZFl::before,
.diversitySelectorOptions-4YM-vX::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-SvZHNd::after,
.emojiPicker-3PwZFl::after,
.diversitySelectorOptions-4YM-vX::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.diversitySelectorOptions-4YM-vX::after,
.diversitySelectorOptions-4YM-vX::before {
	border-radius: 5px;
}
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl {
	box-shadow: unset;
}
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl::after,
.emojiPickerInExpressionPicker-3IzIcv .emojiPicker-3PwZFl::before {
	display: none;
}

.diversityEmojiItem-L6_IXw:hover {							/* picker				diversityemoji						*/
	background-color: rgb(var(--accentcolor));
}

.navButtonActive-1MkytQ {									/* picker				navbuttonactive						*/
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}

.wrapper-2Gsate {											/* picker				sidebar								*/
	background-color: rgba(var(--transparencycolor), .2);
}

.guildIcon-3h-1IH {											/* picker				guildicon							*/
	background-color: rgba(var(--transparencycolor), .2);
}

.categoryItemDefaultCategory-aBZ6nJ:first-child,
.categoryItemDefaultCategory-aBZ6nJ:first-child + .categoryItemDefaultCategory-aBZ6nJ,
.stickerCategoryRecent-1WVWrj {
	margin-bottom: 8px;
}
.categoryItemDefaultCategory-aBZ6nJ:hover,					/* picker				categoryitem						*/
.stickerCategory-3Yz7vN:hover,								/* picker				stickercategoryitem					*/
.stickerCategoryShopWrapper-3EnJdQ:hover .stickerCategoryShop-d5zC3B {
	background-color: rgba(var(--transparencycolor), .3);
}
.categoryItemDefaultCategorySelected-_HCKoz,				/* picker				categoryitem selected				*/
.categoryItemDefaultCategorySelected-_HCKoz:hover,		
.stickerCategorySelected-2uaMAG,							/* picker				stickercategoryitem selected		*/
.stickerCategorySelected-2uaMAG:hover {
	background-color: rgb(var(--accentcolor));
}
.categoryItemDefaultCategorySelected-_HCKoz svg,			/* picker				categoryitem selected				*/
.categoryItemDefaultCategorySelected-_HCKoz:hover svg,
.stickerCategorySelected-2uaMAG svg,						/* picker				stickercategoryitem selected		*/
.stickerCategorySelected-2uaMAG:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.unicodeShortcut-15J8Ck,									/* picker				unicodeemojis shortcut				*/
.stickerCategoryShopWrapper-3EnJdQ {						/* picker				unicodeemojis shortcut				*/
	background-color: transparent;
	border: none;
	overflow: hidden;
	z-index: 100;
}
.unicodeShortcut-15J8Ck:hover {
}
.unicodeShortcut-15J8Ck::before,
.stickerCategoryShopWrapper-3EnJdQ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.unicodeShortcut-15J8Ck::after,
.stickerCategoryShopWrapper-3EnJdQ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.35));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

.inspector-S2gM3e {											/* picker				emojiinfowrapper					*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .wrapper-1-Fsb8 {								/* picker				categoryheader						*/
	background: transparent;
	position: static;
}

#app-mount .imageLoading-bpSr0M {							/* picker				emoji loading						*/
	background: rgba(var(--transparencycolor), .3);
	border-radius: 10px;
}
.emojiItem-14v6tW.emojiItemSelected-1aLkfV {				/* picker				emoji selected						*/
	background-color: rgb(var(--accentcolor));
}
.emojiItemDisabled-1FvFuF {									/* picker				emoji disabled						*/
	filter: none;
	cursor: no-drop;
}
.emojiItemDisabled-1FvFuF > * {
	filter: grayscale(1);
}

.shape-2kfO2v {												/* picker				sticker loading						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.feature-3kpTdS {											/* picker				sticker feature						*/
	background: transparent;
}

.stickerInspected-2EM4w- .stickerBackground-2XECKi {		/* picker				sticker focused						*/
	background-color: rgb(var(--accentcolor));
}
.viewAllBackground-3Bn1vh {									/* picker				sticker view all					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.viewAll-2RLt-n:hover .viewAllBackground-3Bn1vh,
.viewAllInspected-FsmJHj .viewAllBackground-3Bn1vh {
	background-color: rgba(var(--transparencycolor), .4);
}

.premiumPromo-fVlLu- {										/* picker				premium warning						*/
	background-color: transparent;
	opacity: 1;
}
.premiumPromo-fVlLu-::before {
	content: "";
	opacity: 0.9;
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.premiumPromo-fVlLu-::after {
	content: "";
	opacity: 0.9;
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.29));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.premiumPromoClose-1w65km {
	-webkit-mask: url(https://discord.com/assets/f815a774c2b98d3109293a4e2afb733c.svg) 50% 50% no-repeat;
	background: var(--interactive-normal);
}
.premiumPromoClose-1w65km:hover {
	background: var(--interactive-hover);
}
.premiumPromoClose-1w65km:active {
	background: var(--interactive-active);
}
#app-mount .categoryItemDefaultCategorySelected-_HCKoz .categoryIcon-1SvUHG,
#app-mount .categoryItemDefaultCategorySelected-_HCKoz:hover .categoryIcon-1SvUHG {
	color: var(--interactive-active);
}

#app-mount .focused-1En8bG,									/* gifpicker			result								*/
#app-mount .result-3w1ZcL:hover {
	box-shadow: 0 11px 22px 1px rgba(var(--transparencycolor), .3);
}
#app-mount .placeholder-1kJjXI {
	background: rgba(var(--textdarkest),.6);
}
#app-mount .endContainer-1ZDW8j::after {
	background-image: url(https://discord.com/assets/0c735bf91232f2a2266e6ba9d6753565.svg);
	opacity: 0.6;
}
#app-mount .endText-3SrwuD {
	color: var(--header-secondary);
}
#app-mount .emptyHintCard-2mUdMe {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-secondary);
}
#app-mount .backButton-JyKGC1 {								/* gifpicker			backbutton							*/
	color: var(--interactive-normal);
}
#app-mount .backButton-JyKGC1:hover {
	color: var(--interactive-hover);
}
#app-mount .backButton-JyKGC1:active {
	color: var(--interactive-active);
}


/* ----		14.4.	PINS/MENTIONS					---- */

.messagesPopoutWrap-1MQ1bW,								/* popout				wrapper								*/
.container-enaOkj {										/* popout				wrapper	(inbox)						*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	overflow: hidden;
}
.messagesPopoutWrap-1MQ1bW > *,
.container-enaOkj > * {
	z-index: 1000;
}
.messagesPopoutWrap-1MQ1bW::before,
.container-enaOkj::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.messagesPopoutWrap-1MQ1bW::after,
.container-enaOkj::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .messagesPopout-24nkyi {							/* popout				innerwrap							*/
	background-color: transparent;
}

.themedPopout-1TrfdI .header-2Kf7Yu {
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .1);
}
.header-ykumBX {											/* popout				header								*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .2);
}

.themedPopout-1TrfdI .footer-1K57q_ {
	background-color: rgba(var(--transparencycolor), .1);
}
.footer-1kmXd4 {											/* popout				footer								*/
	background-color: rgba(var(--transparencycolor), .2);
}

.messageGroupWrapper-o-Zw7G {
	background-color: transparent;
	border: none;
	overflow: visible;
	padding: 11px 10px 10px 10px;
}
.messageGroupWrapper-o-Zw7G + .messageGroupWrapper-o-Zw7G::before {
	content: "";
	border-top: 1px solid var(--background-modifier-accent);
	position: absolute;
	top: -3px;
	left: 0;
	width: 100%;
}
.messageGroupWrapper-o-Zw7G .contentCozy-3XX413 {
	overflow: hidden;
}
.actionButtons-1sUUug {										/* popout				actionbuttonscontainer				*/
	top: 4px;
	right: 14px;
}
.jumpButton-2dvRSC,											/* popout				jumpbutton (mentions)				*/
.jumpButton-3DTcS_ {										/* popout				jumpbutton (pins)					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.jumpButton-2dvRSC:hover,
.jumpButton-3DTcS_:hover {
	background-color: rgb(var(--accentcolor));
}
.jumpButton-2dvRSC + .jumpButton-2dvRSC,
.jumpButton-3DTcS_ + .jumpButton-3DTcS_ {
	margin-left: 2px;
}
.messageGroupWrapper-o-Zw7G:hover .actionButtons-1sUUug .closeButton-17RIVZ {
	opacity: 1;
}
.hasMoreButton-1MELpI {										/* popout				hasmorebutton						*/
	background-color: rgba(var(--transparencycolor), .2);
	border: none;
}

.image-2JDb81 {												/* popout				emptyimage							*/
	opacity: 0.6;
}

															/* popout				active tab							*/
#app-mount .header-2-Imhb .tabBar-1kuXvJ .tab-ck0077.active-1MbGPa {
	background-color: rgb(var(--accentcolor));
}
.secondary-dIudih,											/* popout				header button						*/
.tertiary-aMXF0g,											/* popout				message button						*/
.collapseButton-3V3Cqh {									/* popout				collapse button						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.secondary-dIudih:hover,
.tertiary-aMXF0g:hover,
.collapseButton-3V3Cqh:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.collapseButton-3V3Cqh {
	position: static;
	margin-left: 12px;
	border-radius: 32px;
	box-sizing: border-box;
	cursor: pointer;
	flex-shrink: 0;
	height: 32px;
	min-height: 32px;
	width: 32px;
	min-width: 32px;
	padding: 8px;
	transform: unset !important;
}
.collapseButton-3V3Cqh.collapsed-b6uSCG svg {
	transform: rotate(-90deg);
}

.channelHeader-3Gd2xq {										/* popout				channelheader						*/
	background-color: rgba(var(--transparencycolor), .4);
	padding-right: 16px;
	border-radius: 5px 5px 0 0;
	position: static;
}
.channelHeader-3Gd2xq:only-child {
	border-radius: 0;
}
.messageContainer-gbhlwo,									/* popout				messagecontainer					*/
.messages-3G3erD {											/* popout				messagecontainer (inbox)			*/
	background-color: rgba(var(--transparencycolor), .2);
	border-radius: 0;
}
.messageContainer-gbhlwo:last-child,
.messages-3G3erD:last-child {
	border-radius: 0 0 5px 5px;
}

.tutorial-3w5I9h {											/* popout				tutorial (inbox)					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.tutorialIcon-3f1miQ {										/* popout				tutorial (inbox)					*/
	background-color: rgba(var(--transparencycolor), .4);
}

/* ----		14.5.	SEARCHPOPOUT					---- */

#app-mount .container-3ayLPN {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	overflow: hidden;
	position: relative;
}
.container-3ayLPN::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-3ayLPN::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .queryContainer-RKFJW- {
	border-bottom-color: var(--background-modifier-accent);
	color: var(--header-secondary);
}
#app-mount .queryContainer-RKFJW- strong {
	color: var(--header-primary);
}
#app-mount .focused-2bY0OD {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .resultsGroup-r_nuzN::before {
	border-top-color: var(--background-modifier-accent);
}
#app-mount .resultsGroup-r_nuzN .header-2N-gMV,
#app-mount .resultsGroup-r_nuzN .plusIcon-v0BTrL,
#app-mount .resultsGroup-r_nuzN .searchClearHistory-2cSSMO,
#app-mount .resultsGroup-r_nuzN .searchLearnMore-3SQUAj a {
	color: var(--text-normal);
}
#app-mount .option-96V44q::after {
	display: none;
}
#app-mount .option-96V44q.selected-rZcOL- {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .option-96V44q.selected-rZcOL-::before {
	background-color: rgb(var(--accentcolor));
	border-radius: 3px;
	width: 34px;
}
#app-mount .option-96V44q .answer-1n6g43,
#app-mount .option-96V44q .nonText-3CRkO0,
#app-mount .option-96V44q strong {
	color: var(--text-normal);
}
#app-mount .option-96V44q .filter-3Y_im- {
	color: var(--text-muted);
}
#app-mount .option-96V44q.user-O3Czj0 .displayedNick-3xxvzU {
	color: var(--text-normal);
}
#app-mount .option-96V44q.user-O3Czj0 .displayUsername-Qekxml {
	color: var(--interactive-muted);
}
#app-mount .searchOption-zQ-1l6 .filter-3Y_im- {
	color: var(--text-normal);
}
#app-mount .searchOption-zQ-1l6 .answer-1n6g43 {
	color: var(--text-muted);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw {
	border-top-color: var(--background-modifier-accent);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hint-165cR4 {
	color: var(--text-normal);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z {
	color: var(--header-primary);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z:hover {
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .searchResultChannelCategory-1l0lSn,
#app-mount .searchResultChannelIcon-1DnTme {
	color: var(--text-muted);
}

#app-mount .calendarPicker-2yf6Ci .react-datepicker {
	background: transparent;
}
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--outside-month) {
	border-color: rgba(var(--transparencycolor), .5);
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--outside-month {
	background: rgba(var(--transparencycolor), .5);
	border-color: transparent;
}
#app-mount .datePicker--XZbmJ .react-datepicker__header,
#app-mount .datePicker--XZbmJ .react-datepicker__month-container,
#app-mount .datePicker--XZbmJ .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	background: rgba(var(--transparencycolor), .2);
}
#app-mount .datePicker--XZbmJ .react-datepicker__header {
	padding-bottom: 5px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation {
	background: transparent;
	border-color: rgba(var(--textbrightest), .5);
	top: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	-webkit-mask: url(https://discord.com/assets/7619529e87dad31fd2ae83d9b9583e49.svg) center/6px 12px no-repeat;
	background-color: rgb(var(--textbrightest));
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation--previous {
	left: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__navigation--next {
	right: 30px;
}
#app-mount .datePicker--XZbmJ .react-datepicker__current-month {
	border-color: transparent;
	padding: 10px 0;
}
#app-mount .datePicker--XZbmJ .react-datepicker__current-month,
#app-mount .datePicker--XZbmJ .react-datepicker__day-name,
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--disabled):hover,
#app-mount .datePicker--XZbmJ .react-datepicker__day:not(.react-datepicker__day--disabled):not(.react-datepicker__day--outside-month),
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hint-165cR4,
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw .hintValue-29ny8Z {
	color: var(--header-primary);
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	color: var(--header-secondary);
}
#app-mount .datePicker--XZbmJ .react-datepicker__day--outside-month {
	color: var(--text-muted);
}
#app-mount .datePicker--XZbmJ .datePickerHint-3Q1Udw {
	margin: 0;
	padding: 20px;
	display: flex;
	justify-content: center;
}

/* ----		14.6.	COLORPICKER						---- */

#app-mount .colorPickerCustom-2CWBn2 {						/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.colorPickerCustom-2CWBn2::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	border-radius: 5px;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.colorPickerCustom-2CWBn2::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.35));
	border-radius: 5px;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		14.7.	ADDROLE							---- */

#app-mount .container-3XJ8ns {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.container-3XJ8ns::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-3XJ8ns::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.focused-dKLoQt,
.item-2J2GlB:hover {
	background: rgba(var(--transparencycolor), .4);
}


/* ----		14.8.	EVERYONEMENTION					---- */

#app-mount .everyonePopout-nEbJY3 {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.everyonePopout-nEbJY3::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.everyonePopout-nEbJY3::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#app-mount .header-3_S6dz {
	color: var(--header-primary);
}
#app-mount .body-2iXqIL {
	color: var(--header-secondary);
}
#app-mount .body-2iXqIL .animation-3GofIz {
	opacity: .5;
}
#app-mount .buttonHint-2OxJB8 {
	color: var(--text-muted);
}
#app-mount .buttonHint-2OxJB8 strong {
	color: var(--header-secondary);
}
#app-mount .footer-2aTx0s {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--text-muted);
}
#app-mount .footer-2aTx0s strong {
	color: var(--header-secondary);
}


/* ----		14.9.	CHANNELFOLLOW					---- */

#app-mount .header-1pGpFt {
	background: rgba(var(--transparencycolor), .3);
}
#app-mount .separator-3gy7tq {
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor), .3), 0 1px 2px 0 rgba(var(--transparencycolor), .3);
}
.channelContainer-1x3D6I {
	background-color: rgba(var(--transparencycolor), .3);
}
.channel-2PJTLY {
	background-color: rgba(var(--transparencycolor), .3);
}
.channelContainer-1x3D6I .channel-2PJTLY {
	background-color: transparent;
}

/* ----		14.10.	CHANNELFOLLOWINFO				---- */

#app-mount .guildPopout-3CgKqR {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.guildPopout-3CgKqR::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.guildPopout-3CgKqR::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		14.11.	EMOJIINFO						---- */

#app-mount .popoutContainer-1MXdqN {						/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.popoutContainer-1MXdqN::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popoutContainer-1MXdqN::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

.emojiSection-3Fb9ix {										/* popout				emojisection						*/
	background-color: transparent;
}

.guildSection-1EoFKd {										/* popout				emojisection						*/
	background-color: rgba(var(--transparencycolor), .2);
}

.loading-1lSwpg {											/* popout				loading placeholder					*/
	background: rgba(var(--transparencycolor), .3);
}

/* ----		14.12.	STREAMPREVIEW					---- */

#app-mount .streamPreview-2-WUWT {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.streamPreview-2-WUWT::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.streamPreview-2-WUWT::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

#app-mount .previewContainer-12UlHl	{						/* popout				preview								*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		14.13.	STREAMINFO						---- */

#app-mount .container-2dqNWc {								/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: visible !important;
}
.container-2dqNWc::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	filter: blur(var(--popoutblur));
	background-attachment: fixed;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-2dqNWc::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		14.14.	PUBLICGUILDANNOUNCEMENT			---- */

#app-mount .popout-6p6fkZ {									/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.popout-6p6fkZ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-6p6fkZ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		14.15.	RTCSTATUSPOPOUT					---- */

#app-mount .container-2x5lvQ {								/* RTCpopout												*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
	position: relative;
	width: 260px;
}
.container-2x5lvQ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
.container-2x5lvQ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
#app-mount .container-2x5lvQ .header-2C89wJ {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#app-mount .container-2x5lvQ canvas {
	background-color: rgb(var(--transparencycolor));
	padding: 5px;
	border-radius: 5px;
}
#app-mount .container-2x5lvQ section {
	background-color: transparent;
}
#app-mount .container-2x5lvQ section p {
	color: var(--header-primary);
}
#app-mount .container-2x5lvQ section strong {
	color: var(--header-primary);
}
#app-mount .debugButton-1Zec0y {
	color: var(--header-secondary);
}
#app-mount .krispLogo-a9msDI {
	-webkit-mask: url(https://discord.com/assets/c28317e203e00b2d7390d5ece2399228.svg) center/contain no-repeat;
	background-color: var(--header-primary);
}

/* ----		14.16.	PHONE-/EMAILVALIDATION			---- */

#app-mount .input-3yHnCz {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#app-mount .phoneFieldPopout-h7c9mt .countryName-3dA1Xv {
	color: var(--header-secondary);
}
#app-mount .phoneFieldPopout-h7c9mt .countryCode-2TeNMX {
	color: var(--header-primary);
}
#app-mount .activityInviteEducationArrow-3DEpKU {
	-webkit-mask: url(https://discord.com/assets/ba018cf9baa19824316dc4c2beb080a4.svg) center/contain no-repeat;
	background: var(--header-primary);
}

#app-mount .emailVerificationModal-3cfLjL .title-38uBel {
	color: var(--header-primary);
}
#app-mount .emailVerificationModal-3cfLjL .body-1_Foxn {
	color: var(--text-muted);
}

#app-mount .verification-3RfWYC .image-2LVZ_j {
	background-image: url(https://discord.com/assets/c290235278e128e94ae5ac37e58c5cbb.svg);
	opacity: .5;
}
#app-mount .verification-3RfWYC .title-wZCcDo {
	color: var(--header-primary);
}
#app-mount .verification-3RfWYC .body-3ROqbj,
#app-mount .verification-3RfWYC .footer-1eZumv {
	color: var(--header-secondary);
}
#app-mount .verificationBlock-1Chfpc {
	background-color: rgba(var(--transparencycolor), .1);
	border: 1px solid rgba(var(--transparencycolor), .3);
}
#app-mount .verificationBlock-1Chfpc:hover {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgb(var(--transparencycolor));
}
#app-mount .verificationBlock-1Chfpc .image-2LVZ_j.email-1MPDs- {
	background-image: url(https://discord.com/assets/cefc9c14adce616059f519c581331b32.svg);
	opacity: .5;
}
#app-mount .verificationBlock-1Chfpc .image-2LVZ_j.phone-27MBJz {
	background-image: url(https://discord.com/assets/ca452f5271ebcc7132db59f60a2a9cfe.svg);
	opacity: .5;
}
#app-mount .verificationBlock-1Chfpc .body-3ROqbj {
	color: var(--header-secondary);
}

/* ----		14.17.	QUICKSELECTPOPOUT				---- */

#app-mount .quickSelectPopout-X1hvgV,						/* quickselect												*/
#app-mount .popoutList-T9CKZQ {								/* listpopout												*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
	position: relative;
}
.quickSelectPopout-X1hvgV::before,
.popoutList-T9CKZQ::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
.quickSelectPopout-X1hvgV::after,
.popoutList-T9CKZQ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
#app-mount .selectableItem-1MP3MQ {
	color: var(--header-primary);
}
#app-mount .selectableItem-1MP3MQ:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .quickSelectPopoutOption-opKBx9:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .quickSelectPopoutOption-opKBx9.selected-3RZo5I {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .popoutListEmpty-voOEBJ {
	color: var(--header-primary);
}
#app-mount .quickSelectArrow-1QublR {
	-webkit-mask: url(https://discord.com/assets/f58cf3b8fc79e9d671ab649ab37651a9.svg) 50% no-repeat;
	background: var(--interactive-normal);
}

/* ----		14.18.	WARNINGPOPOUT					---- */

#app-mount .contentWarningPopout-n5JsIs {					/* popout													*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
}
.contentWarningPopout-n5JsIs::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
.contentWarningPopout-n5JsIs::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	pointer-events: none;
	border-radius: 5px;
	z-index: -1;
}
#app-mount .body-3PNusm {
	color: var(--header-secondary);
}
#app-mount .header-2NYWtG {
	color: var(--header-primary);
}


/* ~~~~		15.		GENERAL							~~~~ */

::selection {												/* selection												*/
	background: rgb(var(--accentcolor));
}
.highlight {
	background: rgb(var(--accentcolor));
}

#app-mount .elevationLow-2lY09M, #app-mount .elevationLow-126AxN, .lightElevationLow-3_Ybxi, .darkElevationLow-DABD7i {
	box-shadow: 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .elevationHigh-3A9Xbf, #app-mount .elevationHigh-1PneE4, .lightElevationHigh-3usmGv, .darkElevationHigh-6iWpWi {
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .elevationBorderLow-2qgTRQ, #app-mount .elevationBorderLow-2_BGCd, .lightElevationBorderLow-3APXjz, .darkElevationBorderLow-39dDV7 {
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .elevationBorderHigh-2WYJ09, #app-mount .elevationBorderHigh-2_BGCd, .lightElevationBorderHigh-2T98IF, .darkElevationBorderHigh-2U1nXW {
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}

#app-mount .breadcrumbWrapper-WmDjgG {						/* breadcrumbs			wrapper							*/
	color: rgba(var(--textbrightest),.3);
}
#app-mount .activeBreadcrumb-p6aw-F {						/* breadcrumbs			active							*/
	color: rgba(var(--textbrightest),.6);
}

/* ----		15.1.	TEXT							---- */

.description-1u9Qui {
	color: var(--header-secondary);
}

#app-mount h1.title-3KTIjF,
#app-mount h2.title-3KTIjF {
	color: var(--header-primary);
}
#app-mount h3.title-3KTIjF {
	color: var(--text-normal);
}
#app-mount h4.title-3KTIjF,
#app-mount h5.title-3KTIjF,
#app-mount h6.title-3KTIjF {
	color: var(--header-secondary);
}

#app-mount .text-GwUZgS,
#app-mount .title-2BxgL2 {
	color: var(--text-muted);
}

#app-mount .title-3pjxZQ {
	color: var(--header-secondary);
}

#app-mount .markdown-11q6EU {
	color: var(--text-normal);
}
#app-mount .markdown-11q6EU th {
	background-color: var(--background-tertiary);
	border-color: var(--interactive-muted);
	color: var(--header-primary);
}
#app-mount .markdown-11q6EU td {
	border-color: var(--interactive-muted);
}
#app-mount .markdown-11q6EU tr {
	border-color: var(--interactive-muted);
	color: var(--header-secondary);
}
#app-mount .markdown-11q6EU tr:nth-child(2n) {
	background-color: var(--background-secondary);
}
#app-mount .markdown-11q6EU .blockquote-2-nEPK {
	border-left-color: var(--interactive-muted);
}
#app-mount .markdown-11q6EU code {
	background-color: var(--background-secondary);
}
#app-mount .markdown-11q6EU .codeInline-1FHKS7 {
	color: var(--text-normal);
}

/* ----		15.2.	BUTTONS							---- */

.btn-1PnLxm.btnPrimary-1jluZW,
.lookFilled-1Gx00P.hoverBrand-1_Fxlk.hasHover-3X1-zV:hover,
.lookFilled-1Gx00P.colorBrand-3pXr91:not(.buttonColor-7qQbGO):not([style*="background-color"]) {
	text-shadow: 1px 1px var(--textshadow);
}
.lookFilled-1Gx00P.hoverBrand-1_Fxlk.hasHover-3X1-zV:hover svg,
.lookFilled-1Gx00P.colorBrand-3pXr91:not(.buttonColor-7qQbGO):not([style*="background-color"]) svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

#app-mount .lookInverted-2D7oAl.colorPrimary-3b3xI6 .spinnerItem-3GlVyU {
	background-color: rgb(var(--textdarkest));
}
#app-mount .lookOutlined-3sRXeN.colorPrimary-3b3xI6 .spinnerItem-3GlVyU,
#app-mount .lookLink-9FtZy-.colorPrimary-3b3xI6 .spinnerItem-3GlVyU {
	background-color: rgb(var(--textdarkest));
}

#app-mount .lookFilled-1Gx00P.colorPrimary-3b3xI6:hover,
#app-mount .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .lookFilled-1Gx00P.colorPrimary-3b3xI6:active,
#app-mount .lookFilled-1Gx00P.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-color: rgba(var(--transparencycolor), .6);
}
#app-mount .lookFilled-1Gx00P.colorPrimary-3b3xI6,
#app-mount .lookFilled-1Gx00P.colorPrimary-3b3xI6:disabled {
	background-color: rgba(var(--transparencycolor), .2);
	color: #FFF;
}

#app-mount .lookInverted-2D7oAl.colorPrimary-3b3xI6:hover,
#app-mount .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	background-image: linear-gradient(0deg, rgba(0, 0, 0, .1), rgba(0, 0, 0, .1));
}
#app-mount .lookInverted-2D7oAl.colorPrimary-3b3xI6:active,
#app-mount .lookInverted-2D7oAl.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-image: linear-gradient(0deg, rgba(0, 0, 0, .2), rgba(0, 0, 0, .2));
}
#app-mount .lookInverted-2D7oAl.colorPrimary-3b3xI6,
#app-mount .lookInverted-2D7oAl.colorPrimary-3b3xI6:disabled {
	background-color: #FFF;
	color: rgba(var(--textdarkest));
}

#app-mount .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover {
	border-color: rgba(var(--textdarkest), .6);
}
#app-mount .lookOutlined-3sRXeN.hoverPrimary-2D1j2r.hasHover-3X1-zV:active {
	background-color: rgba(var(--textdarkest), .1);
	border-color: rgb(var(--textdarkest));
}
#app-mount .lookOutlined-3sRXeN.colorPrimary-3b3xI6,
#app-mount .lookOutlined-3sRXeN.colorPrimary-3b3xI6:disabled {
	border-color: rgba(var(--textdarkest), .1);
	color: rgb(var(--textdarkest));
}

#app-mount .lookLink-9FtZy-.colorPrimary-3b3xI6 {
	color: rgb(var(--textdarkest));
}
#app-mount .lookLink-9FtZy-.colorPrimary-3b3xI6:hover .contents-18-Yxp,
#app-mount .lookLink-9FtZy-.hoverPrimary-2D1j2r.hasHover-3X1-zV:hover .contents-18-Yxp {
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--textdarkest)) 0, rgb(var(--textdarkest)) 2px, transparent 0);
	color: rgb(var(--textdarkest));
}

#app-mount .lookInverted-2D7oAl.colorTransparent-1ewNp9 .spinnerItem-3GlVyU {
	background-color: rgba(var(--textbrightest),.1);
}
#app-mount .lookFilled-1Gx00P.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
#app-mount .lookOutlined-3sRXeN.colorTransparent-1ewNp9 .spinnerItem-3GlVyU,
#app-mount .lookLink-9FtZy-.colorTransparent-1ewNp9 .spinnerItem-3GlVyU {
	background-color: var(--header-primary);
}

#app-mount .lookFilled-1Gx00P.colorTransparent-1ewNp9:hover,
#app-mount .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--textbrightest),.05);
}
#app-mount .lookFilled-1Gx00P.colorTransparent-1ewNp9:active,
#app-mount .lookFilled-1Gx00P.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active  {
	background-color: rgba(var(--textbrightest),.01);
}
#app-mount .lookFilled-1Gx00P.colorTransparent-1ewNp9,
#app-mount .lookFilled-1Gx00P.colorTransparent-1ewNp9:disabled {
	background-color: rgba(var(--textbrightest),.1);
	color: var(--header-primary);
}

#app-mount .lookInverted-2D7oAl.colorTransparent-1ewNp9:hover,
#app-mount .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--textbrightest),.05);
}
#app-mount .lookInverted-2D7oAl.colorTransparent-1ewNp9:active,
#app-mount .lookInverted-2D7oAl.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--textbrightest),.1);
}
#app-mount .lookInverted-2D7oAl.colorTransparent-1ewNp9,
#app-mount .lookInverted-2D7oAl.colorTransparent-1ewNp9:disabled  {
	background-color: var(--header-primary);
	color: rgba(var(--textbrightest),.1);
}

#app-mount .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover {
	background-color: rgba(var(--textbrighter),.1);
	border-color: var(--interactive-hover);
}
#app-mount .lookOutlined-3sRXeN.hoverTransparent-2Lz5CN.hasHover-3X1-zV:active {
	background-color: rgba(var(--textbrightest),.1);
	border-color: var(--header-primary);
}
#app-mount .lookOutlined-3sRXeN.colorTransparent-1ewNp9,
#app-mount .lookOutlined-3sRXeN.colorTransparent-1ewNp9:disabled {
	background-color: transparent;
	color: var(--text-normal);
}

#app-mount .lookLink-9FtZy-.colorTransparent-1ewNp9 {
	color: var(--text-normal);
}
#app-mount .lookLink-9FtZy-.colorTransparent-1ewNp9:hover .contents-18-Yxp,
#app-mount .lookLink-9FtZy-.hoverTransparent-2Lz5CN.hasHover-3X1-zV:hover .contents-18-Yxp {
	background-image: linear-gradient(0deg, transparent,transparent 1px,rgb(var(--textbrighter)) 0,rgb(var(--textbrighter)) 2px,transparent 0);
	color: var(--text-normal);
}

/* ----		15.3.	INPUTS							---- */

.input-cIJ7To {												/* valueinput			bordered							*/
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
.input-cIJ7To:hover:not(:focus) {
	border-color: rgb(var(--transparencycolor));
}

#app-mount .prefixInput-14nUik {
	background-color: rgba(0,0,0,.1);
	border-color: rgba(0,0,0,.3);
}
#app-mount .prefixInput-14nUik:hover {
	border-color: rgba(0,0,0,.6);
}
#app-mount .prefixInputInput-cqxbLV {
	color: var(--header-primary);
}
#app-mount .prefixInputInput-cqxbLV::-webkit-input-placeholder,
#app-mount .prefixInputInput-cqxbLV::-moz-placeholder,
#app-mount .prefixInputInput-cqxbLV:-ms-input-placeholder,
#app-mount .prefixInputInput-cqxbLV::placeholder {
	color: var(--text-muted);
}
#app-mount .prefixInputPrefix-2IUJ4X {
	color: var(--text-muted);
}

#app-mount .maxLength-39QFBo {
	color: var(--text-muted);
}

#app-mount .copyInput-2rOSt7 {
	background-color: var(--deprecated-text-input-bg);
}
#app-mount .copyInputDefault-21sXtF {
	border-color: var(--deprecated-text-input-border);
}
#app-mount .hiddenMessage-1iiFV5,
#app-mount .inputDefault-A2ud2y {
	color: var(--header-primary);
}
#app-mount .hiddenMessage-1iiFV5::placeholder,
#app-mount .inputDefault-A2ud2y::placeholder {
	color: rgba(var(--textbrightest),.3);
}

.container-3auIfb {											/* checkboxswitch											*/
	background-color: rgba(var(--transparencycolor), .3) !important;
}
.container-3auIfb rect[fill] {
	fill: var(--header-primary) !important;
}
.container-3auIfb path[fill] {
	fill: rgb(var(--transparencycolor)) !important;
}

#app-mount .item-26Dhrx {									/* radiogroup			container							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .item-26Dhrx:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .item-26Dhrx[aria-checked=true] .radioBar-bMNUI- {
	background: rgb(var(--accentcolor));
}
#app-mount .item-26Dhrx[aria-checked=true] .radioBar-bMNUI- .radioIconForeground-XwlXQN {
	color: var(--header-primary);
}
#app-mount .item-26Dhrx .radioBar-bMNUI-[style*="--radio-bar-accent-color"] {
	background: var(--radio-bar-accent-color);
	border: unset;
	color: var(--header-primary);
}
#app-mount .item-26Dhrx[aria-checked=false]:hover .radioBar-bMNUI-[style*="--radio-bar-accent-color"] {
	background: var(--radio-bar-accent-color) linear-gradient(to right, rgba(255, 255, 255, .2), rgba(255, 255, 255, .2));
}

#app-mount .checkboxContainer-2vV9zd::before {				/* checkbox				container							*/
	background-color: rgba(var(--textdarker), .3);
}
#app-mount .checkbox-1ix_J3 {								/* checkbox				inner								*/
	border-color: rgb(var(--textdark));
}
#app-mount .checkbox-1ix_J3.checked-3_4uQ9 {				/* checkbox				checked								*/
	background-color: rgb(var(--textbrightest));
	border-color: rgb(var(--textbrightest));
}
#app-mount .checkbox-1ix_J3.checked-3_4uQ9.round-2jCFai {	/* checkbox				roundchecked						*/
	background-color: rgb(var(--accentcolor)) !important;
	border-color: rgb(var(--accentcolor)) !important;
}
#app-mount .checkbox-1ix_J3.checked-3_4uQ9.round-2jCFai svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}
#app-mount .checkbox-1ix_J3.checked-3_4uQ9.round-2jCFai path[fill] {
	fill: #fff;
}
.checkboxMute-14hTGS::before {
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .bar-2Qqk5Z {									/* slider				backgroundbar						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.grabber-3mFHz2 {											/* slider				grabber								*/
	background-color: var(--header-primary);
	border-color: var(--header-primary);
	box-shadow: 0 3px 1px 0 rgba(var(--transparencycolor), .05), 0 2px 2px 0 rgba(var(--transparencycolor), .1), 0 3px 3px 0 rgba(var(--transparencycolor), .05);
}
#app-mount .markValue-2DwdXI {								/* slider				markvalue							*/
	color: var(--text-muted);
}
#app-mount .defaultValue-3gC7yw .markValue-2DwdXI {
	color: #43b581;
}
#app-mount .markDash-3hAolZ {
	background: transparent;
	color: rgba(var(--transparencycolor), .3);
}
#app-mount .defaultValue-3gC7yw .markDash-3hAolZ {
	color: #43b581;
}
#app-mount .markDash-3hAolZ::before,
#app-mount .markDash-3hAolZ::after {
	content: "";
	position: absolute;
	background: currentColor;
	height: 8px;
	width: 2px;
}
#app-mount .markDash-3hAolZ::before {
	top: 14px;
}
#app-mount .markDash-3hAolZ::after {
	top: 30px;
}
#app-mount .bubble-3we2di {									/* slider				bubble								*/
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .bubble-3we2di::before {
	border-top-color: rgb(var(--accentcolor));
}

#app-mount .container-1nZlH6 {								/* hotkeyinput			container							*/
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
#app-mount .editIcon-13gaox {								/* hotkeyinput			editicon							*/
	-webkit-mask: url(https://discord.com/assets/860396b3ff3fa1c4ae355bebfabadecb.svg) center/cover no-repeat;
	background: var(--header-primary);
}
#app-mount .container-CpszHS.recording-1H2dS7 .button-34kXw5 {
	background-color: rgba(var(--dangercolor)),.1);
	color: rgb(var(--dangercolor));
}

.select-2TCrqx [class*="css-"][class*="-container"] {		/* select				container							*/
	background-color: transparent;
}
.lookFilled-22uAsw.select-2fjwPw,
.select-2TCrqx [class*="css-"][class*="-control"] {
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
.lookFilled-22uAsw.select-2fjwPw:hover.open-kZ53_U,
.lookFilled-22uAsw.open-kZ53_U {
	border-color: rgb(var(--transparencycolor)) rgb(var(--transparencycolor)) rgba(var(--transparencycolor), .3);
}
.lookFilled-22uAsw.select-2fjwPw .searchInput-5YMkDH {
	background: transparent;
}
.select-2fjwPw,
.select-2TCrqx [class*="css-"][class*="-control"] {
	background-color: var(--deprecated-text-input-bg);
	border-color: var(--deprecated-text-input-border);
	color: var(--text-normal);
}
.select-2TCrqx [class*="css-"][class*="-control"]:hover,
.select-2TCrqx [class*="css-"][class*="-control"]:not(:last-child) {
	border-color: var(--deprecated-text-input-border-hover);
}
.select-2TCrqx.languageSelector-LEtpHP [class*="css-"][class*="-control"] {
	background-color: rgba(var(--transparencycolor), .3);
}
.select-2TCrqx [class*="css-"][class*="-singleValue"],
.select-2TCrqx [class*="css-"][class*="-placeholder"],
.select-2TCrqx [class*="css-"][class*="-indicatorContainer"] {
	color: var(--text-normal);
}
.selectedIcon-3uS11H {
	color: var(--interactive-active);
}
#app-mount .optionNormal-12VR9V,
.css-1gfjib6-option,
.css-1yz4bi9-option,
.css-ru8b0x-option,
.css-1yz4bi9-option {
	background-color: rgba(var(--transparencycolor), .1);
	color: var(--interactive-normal);
}
#app-mount .optionNormal-12VR9V:hover,
.css-pkcurw-option,
.css-rzbxvl-option,
.css-1qxn4c5-option,
.css-rzbxvl-option {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--interactive-hover);
}
#app-mount .optionActive-KkAdqq,
.css-1gxgi19-option,
.css-1ba14n5-option,
.css-6qzljd-option,
.css-1ba14n5-option {
	background-color: rgba(var(--transparencycolor), .5);
	color: var(--interactive-active);
}
.role-3ulsK-:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.popout-VcNcHB::-webkit-scrollbar {
	display: none;
}
.popout-VcNcHB,
.container-3LUQwT,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"] {
	background-color: transparent;
	border: 1px solid rgba(var(--transparencycolor), .3);
	box-shadow: 0px 1px 5px 0px rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
.popout-VcNcHB .content-3YMskv::before,
.container-3LUQwT::before,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-VcNcHB .content-3YMskv::after,
.container-3LUQwT::after,
.select-2TCrqx > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}

/* ----		15.4.	SEARCHBARS						---- */

.container-2XeR5Z,											/* searchbar			inner								*/
.container-cMG81i {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .searchBox-3Y2Vi7 .searchBoxInput-uJtBcv::placeholder {
	color: var(--text-muted);
}
#app-mount .searchIcon-1a1-yA {
	color: var(--text-muted);
}
#app-mount .filterLabel-2yQNPl {
	color: var(--header-secondary);
}
#app-mount .searchBox-3Y2Vi7:not(.searchBox-2_mAlO) {
	background-color: rgba(var(--transparencycolor), .3);
	box-shadow: 0 2px 5px 0 rgba(var(--transparencycolor), .2);
}

/* ----		15.5.	TAGS							---- */

.botTagRegular-2HEhHi:not([style]) {						/* bottag				regular								*/
	text-shadow: 1px 1px var(--textshadow);
}
.botTagRegular-2HEhHi:not([style]) svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.base-PmTxvP[style*="var(--bdfdb-blurple)"],				/* numberbadge												*/
.base-PmTxvP[style*="background-color: rgb(88, 101, 242)"],
.base-PmTxvP[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--textshadow);
}

.iconBadge-2wi9r4 {											/* iconbadge												*/
	background-color: rgba(var(--transparencycolor), .3);
}

/* ----		15.6.	ICONS							---- */

.emptySearchImage-1qOMLW,									/* empty search												*/
.image-1GzsFd {												/* no peoples/webhooks/etc.									*/
	opacity: 0.6;
}

#app-mount .invalidPoop-pnUbq7 {							/* erroricon			invalidpoop							*/
	background-color: rgba(var(--transparencycolor), .3);
	opacity: 0.7;
}
#app-mount .guildIconExpired-2Qcq05 {						/* erroricon			expiredguild						*/
	background-color: rgba(var(--transparencycolor), .3);
	opacity: 0.7;
}

/* ----		15.7.	SCROLLBARS						---- */

::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar {
	width: 8px;
	height: 8px;
}
#app-mount .scroller-3vODG7::-webkit-scrollbar {
	width: 6px;
	height: 6px;
}
#app-mount .scroller--qpKGq::-webkit-scrollbar,
#app-mount .scrollbar-3dvm_9::-webkit-scrollbar,
#app-mount .scroller-2PSBSf::-webkit-scrollbar {
	width: 4px;
	height: 4px;
}
::-webkit-scrollbar,
::-webkit-scrollbar-track,
::-webkit-scrollbar-track-piece,
#app-mount ::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar-track,
#app-mount ::-webkit-scrollbar-track-piece {
	border-color: transparent !important;
	background: transparent !important;
}
::-webkit-scrollbar-thumb,
#app-mount ::-webkit-scrollbar-thumb {
	border-radius: 10px;
	border: none;
	background-color: rgb(var(--accentcolor)) !important;
}
.none-2Eo-qx::-webkit-scrollbar-corner,
.none-2Eo-qx::-webkit-scrollbar-thumb,
.none-2Eo-qx::-webkit-scrollbar-track,
.none-2Eo-qx::-webkit-scrollbar {
	display: none;
}

/* ----		15.8.	NOTIFICATIONBAR					---- */

.base-3dtUhz .notice-3bPHh- {
	border-radius: 0;
}
#app-mount .notice-2FJMB4 {
	box-shadow: 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .notice-2X5hT5 {
	background-color: rgba(var(--transparencycolor), .6);
}
.noticeBrand-3nQBC_ {
	text-shadow: 1px 1px var(--textshadow);
}
.noticeBrand-3nQBC_ .button-1MICoQ {
	box-shadow: 1px 1px var(--textshadow);
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		15.9.	TOOLTIPS						---- */

.headerText-1e7ZU0,
.bodyText-3yi6Dj {
	color: #fff;
}
#app-mount .tooltip-3oByQd,
#app-mount .tooltip-1_vJJI,
#app-mount .tooltip-2QfLtc {
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: #fff;
}
#app-mount .guildNameText-74xXQn {
	color: #fff;
}
#app-mount .muteText-1DPH3L {
	color: #bbb;
}
#app-mount .tooltip-3oByQd,
#app-mount .tooltip-1_vJJI,
#app-mount .tooltipPrimary-1d1ph4,
#app-mount .tooltipGrey-1hnvTt,
#app-mount .tooltipBlack-PPG47z {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .tooltipPrimary-1d1ph4 .note-e4Jh6_,
#app-mount .tooltipGrey-1hnvTt .note-e4Jh6_,
#app-mount .tooltipBlack-PPG47z .note-e4Jh6_ {
	color: #bbb;
}
#app-mount .tooltipPrimary-1d1ph4 .tooltipPointer-3ZfirK,
#app-mount .tooltipGrey-1hnvTt .tooltipPointer-3ZfirK,
#app-mount .tooltipBlack-PPG47z .tooltipPointer-3ZfirK {
	border-top-color: rgb(var(--accentcolor));
}
#app-mount .tooltipPointer-22Q7m0,
#app-mount .tooltipPointer-1awMxk {
	border-right-color: rgb(var(--accentcolor));
}
.emptyUser-7txhlW {
	background: rgba(var(--transparencycolor), .5);
}
.moreUsers-7v8yWY {
	background: rgba(var(--transparencycolor), .5);
}


/* ~~~~		16.		BDSUPPORT						~~~~ */

html .bd-toast {
	background-color: rgb(var(--accentcolor));
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
html .bd-toast.icon {
	background-image: none !important;
}
html .bd-toast.icon::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: #fff !important;
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg"><path fill="black" d=""/></svg>') center/cover no-repeat;
}
html .bd-toast.toast-danger.icon::before,
html .bd-toast.toast-error.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="black" d="M12 2C6.47 2 2 6.47 2 12s4.47 10 10 10 10-4.47 10-10S17.53 2 12 2zm5 13.59L15.59 17 12 13.41 8.41 17 7 15.59 10.59 12 7 8.41 8.41 7 12 10.59 15.59 7 17 8.41 13.41 12 17 15.59z"/></svg>') 6px 50%/20px 20px no-repeat;
}
html .bd-toast.toast-info.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="black" d="M 12 2 C 6.48 2 2 6.48 2 12 s 4.48 10 10 10 10-4.48 10-10 S 17.52 2 12 2 z m 1 15 h -2 v -6 h 2 v 6 z m 0-8 h -2 V 7 h 2 v 2 z"/></svg>') 6px 50%/20px 20px no-repeat;
}
html .bd-toast.toast-success.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="black" d="M 12 2 C 6.48 2 2 6.48 2 12 s 4.48 10 10 10 10-4.48 10-10 S 17.52 2 12 2 z m -2 15 l -5-5 1.41-1.41 L 10 14.17 l 7.59-7.59 L 19 8 l -9 9 z"/></svg>') 6px 50%/20px 20px no-repeat;
}
html .bd-toast.toast-warning.icon::before,
html .bd-toast.toast-warn.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="black" d="M 1 21 h 22 L 12 2 1 21 z m 12-3 h -2 v -2 h 2 v 2 z m 0-4 h -2 v -4 h 2 v 4 z"/></svg>') 6px 50%/20px 20px no-repeat;
}

#app-mount .fav {
	background: var(--interactive-active);
	width: 16px;
	height: 16px;
	padding: 0;
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/fav_star_empty.svg) center/contain no-repeat;
}
#app-mount .fav:hover,
#app-mount .fav.active {
	background: #faa61a;
}
#app-mount .fav.active {
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/fav_star.svg) center/contain no-repeat;
}

#app-mount .bd-tab-item:hover {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .bd-tab-item.selected {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .bd-server-card {								/* pubslayer			guildcard							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .bd-server-icon {								/* pubslayer			guildicon							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: transparent;
}
#app-mount .bd-server-card:hover,
#app-mount .bd-server-icon:hover {
	background-color: rgba(var(--transparencycolor), .4);
}

.bd-switch-body {											/* bd switch												*/
	--switch-color: rgb(var(--transparencycolor));
	background-color: rgba(var(--transparencycolor), .3);
}

.bd-select .bd-select-options {								/* bd select			popout								*/
	background-color: transparent;
	border: none;
	border-radius: 4px;
	box-shadow: rgba(var(--transparencycolor), .3) 0px 2px 5px 0px;
	box-sizing: border-box;
	padding: 6px 8px;
	margin-left: -9px;
}
.bd-select .bd-select-options::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.bd-select .bd-select-options::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.3));
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.bd-select .bd-select-option {								/* bd select			popout option						*/
	display: flex;
	align-items: center;
	min-height: 32px;
	border-radius: 2px;
	box-sizing: border-box;
	color: var(--interactive-normal);
	font-size: 14px;
	font-weight: 500;
	line-height: 18px;
	margin-top: 2px;
	margin-bottom: 2px;
	padding: 0 8px;
}
.bd-select .bd-select-option:hover {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--interactive-hover);
}
.bd-select .bd-select-option.selected {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--interactive-active);
}

.bd-pfbtn {													/* addonlist			folder button						*/
	text-shadow: 1px 1px var(--textshadow);
}

.bd-server-tag {											/* addonlist			public list tag						*/
	text-shadow: 1px 1px var(--textshadow);
}

.bd-addon-views .bd-view-button:hover {
	background-color: rgba(var(--transparencycolor), .3);
}

.bd-button {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.bd-button.bd-button-danger {
	filter: unset;
}

.floating-window.resizable {								/* customcss editor		detached							*/
	background: rgb(var(--transparencycolor));
}
html .monaco-editor .reference-zone-widget .ref-tree .referenceMatch .highlight {
	background: rgb(var(--accentcolor));
}


/* ~~~~		17.		POWERCORDSUPPORT				~~~~ */

html .powercord-toast {
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
html .powercord-toast::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
html .powercord-toast::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
html .powercord-toast .header {
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
html .powercord-toast .contents .inner {
	background-color: rgba(var(--transparencycolor), .2);
	border: none;
	color: var(--header-secondary);
}


/* ~~~~		18.		PLUGINSUPPORT					~~~~ */

/* ----		18.1.	BDFDB							---- */

html .colorDefault-XdNdIp .bg-8df5St {
	background: linear-gradient(rgba(var(--transparencycolor), .75), rgba(var(--transparencycolor), .75))  var(--popoutposition)/var(--popoutsize), var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
}

/* ----		18.2.	DATEVIEWER						---- */

#app-mount #dv-mount {
	background: transparent;
	z-index: 1;
}
#app-mount #dv-mount::after,
#app-mount #dv-mount::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
#app-mount #dv-mount::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--memberlisttransparency) * 0.85));
}
#app-mount #dv-mount::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
}
#app-mount #dv-main {
	border-top-color: rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#app-mount #dv-main .dv-date {
	color: var(--header-secondary);
	opacity: 1;
}

/* ----		18.3.	MEMBERCOUNT						---- */

#app-mount #MemberCount {
	background-color: transparent;
	width: calc(100% - 8px);
	margin: 0;
	line-height: 0;
	height: 30px;
}
#MemberCount::after,
#MemberCount::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
#MemberCount::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--memberlisttransparency) * 0.85));
}
#MemberCount::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	filter: blur(var(--backgroundblur));
}

/* ----		18.4.	LINENUMBERS						---- */

.hljs ol li {
	border-left-color: var(--background-modifier-accent);
}
.hljs ol li::before {
	color: rgb(var(--textdarker));
}

/* ----		18.5.	PERMISSIONVIEWER				---- */

#permissions-modal-wrapper #permissions-modal {				/* modal				container							*/
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
#permissions-modal-wrapper #permissions-modal::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#permissions-modal-wrapper #permissions-modal::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
#permissions-modal-wrapper .header {
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#permissions-modal-wrapper .modal-body {
	background-color: transparent;
}
#permissions-modal-wrapper .scroller-title {
	border-bottom: 1px solid rgba(var(--transparencycolor), .3);
}
#permissions-modal-wrapper .role-side {
	background-color: rgba(var(--transparencycolor), .1);
}
#permissions-modal-wrapper .role-item {
	color: var(--text-normal);
}
#permissions-modal-wrapper .role-item:hover {
	background-color: rgba(var(--transparencycolor), .1);
}
#permissions-modal-wrapper .role-item.selected {
	background-color: rgba(var(--transparencycolor), .2);
}
#permissions-modal-wrapper .perm-side {
	background-color: transparent;
}
#permissions-modal-wrapper .perm-item {
	box-shadow: inset 0 -1px 0 var(--background-modifier-accent);
}
#permissions-modal-wrapper .perm-name {
	color: var(--header-secondary);
}

/* ----		18.6.	DIRECTDOWNLOAD					---- */

#files_directDownload .file {
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--accentcolor), .2);
	border-radius: 6px 6px 0 0;
}
#files_directDownload .file svg {
	fill: var(--interactive-active);
	opacity: 0.5;
}
#files_directDownload .file svg:hover {
	opacity: 1;
}
#files_directDownload .file span {
	color: var(--header-primary);
}
#files_directDownload .file .progress-bar {
	background-color: rgb(var(--accentcolor));
}

/* ----		18.7.	BETTERFORMATINGREDUX			---- */

.innerDisabled-2mc-iF ~ .bf-toolbar {
	display: none;
}
.bf-arrow {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24"><path fill="black" d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z"/></svg>') center/contain no-repeat;
	background: var(--interactive-active) !important;
}
.bf-toolbar {
	background: transparent;
	overflow: hidden;
	transform: none;
	top: -50px;
}
.bf-toolbar::after {	
	content: "";
	display: block;
	position: absolute;
	width: 100%;
	height: calc(100% - 15px);
	pointer-events: none;
	left: 0px;
	top: 5px;
	background-color: rgba(var(--transparencycolor), .5);
	border-radius: 3px;
	transform: translate(0, 55px);
	transition: all 200ms ease;
	z-index: 200;
}
.bf-toolbar.bf-visible::after,
.bf-toolbar.bf-hover:hover::after {
	transform: translate(0, 0);
	transition: all 200ms cubic-bezier(0,0,0,1);
}
.bf-toolbar::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	z-index: 100;
}
.theme-brand .bf-toolbar::after {
	background: rgb(var(--accentcolor)) linear-gradient(rgba(var(--transparencycolor), .2), rgba(var(--transparencycolor), .2)) !important;
}
.theme-brand .bf-toolbar::before {
	display: none;
}
.bf-toolbar > * {
	z-index: 300;
}
.bf-toolbar .format {
	color: var(--text-normal);
}
.bf-toolbar .format:hover {
	background-color: rgb(var(--accentcolor));
	color: #fff;
}

/* ----		18.8	CHANNELHISTORY					---- */

.channelHistoryButtons {
	top: 4px;
	left: 310px;
}

/* ----		18.9	CHANNELTABS						---- */

html .channelTabs-tabContainer,
html .channelTabs-favContainer {
	display: flex;
	align-items: center;
	flex-wrap: wrap;
	min-height: 28px;
	height: unset;
	overflow: hidden;
	transition: height 0.3s linear;
}
html .channelTabs-tabContainer {
	background: rgba(var(--transparencycolor), calc(0.05 + var(--guildchanneltransparency) * 2));
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
	padding-top: 6px;
}
html .channelTabs-favContainer {
	background: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 2));
	padding-top: 3px;
	padding-bottom: 3px;
}
html .channelTabs-noFavs {
	background: transparent;
	padding: 0 6px;
}

html .channelTabs-tab,
html .channelTabs-fav {
	display: flex;
	align-items: center;
	color: var(--interactive-normal);
	height: 28px;
	margin: 0 4px;
	padding: 0 4px;
	cursor: pointer;
}
html .channelTabs-tab {
	background: rgba(var(--transparencycolor), .3);
	border-radius: 5px 5px 0 0;
}
html .channelTabs-tab:not(.channelTabs-selected):hover,
html .channelTabs-fav:hover {
	background: rgba(var(--transparencycolor), .4);
	color: var(--interactive-hover);
}
html .channelTabs-tab.channelTabs-selected,
html .channelTabs-fav:active {
	background: rgb(var(--accentcolor));
	color: var(--interactive-active);
}
html .channelTabs-tab > *,
html .channelTabs-fav > *,
html .channelTabs-tab .channelTabs-mentionBadge,
html .channelTabs-fav .channelTabs-mentionBadge,
html .channelTabs-tab .channelTabs-unreadBadge,
html .channelTabs-fav .channelTabs-unreadBadge {
	position: static !important;
	transform: unset !important;
	float: unset !important;
}
html .channelTabs-tabIcon,
html .channelTabs-favIcon {
	margin-right: 6px !important;
}
html .channelTabs-tabName,
html .channelTabs-favName {
	margin: 0 !important;
	font-size: 16px;
	line-height: 20px;
	font-weight: 500;
	white-space: nowrap;
}
html .channelTabs-tab .channelTabs-tabName ~ *,
html .channelTabs-fav .channelTabs-favName ~ * {
	margin: 0 0 0 4px !important;
}
html .channelTabs-closeTab,
html .channelTabs-tab.channelTabs-selected .channelTabs-closeTab {
	position: static;
	background: rgba(var(--transparencycolor), .3);
	color: var(--interactive-hover);
	border-radius: 50%;
	width: 14px;
	height: 14px;
	min-width: 14px;
	min-height: 14px;
	font-size: 14px;
	line-height: unset;
}
html .channelTabs-closeTab:hover,
html .channelTabs-tab.channelTabs-selected .channelTabs-closeTab:hover {
	background: #f04747;
	color: var(--interactive-active);
}
html .channelTabs-newTab {
	position: static;
	display: flex;
	justify-content: center;
	align-items: center;
	background: rgba(var(--transparencycolor), .3);
	color: var(--interactive-hover);
	padding: 0;
	width: 22px;
	height: 22px;
}
html .channelTabs-newTab:hover {
	background: rgb(var(--accentcolor));
	color: var(--interactive-active);
}

/* ----		18.10	TYPINGINDICATOR					---- */

html .typingindicator-guild,
html .typingindicator-dms,
html .typingindicator-folder {
	background: rgb(var(--transparencycolor), .2);
	border: 4px solid rgb(var(--transparencycolor), .2);
	box-shadow: unset;
	right: 8px;
	bottom: -5px;
	padding: 2px 0;
}

/* ----		18.11	BADGESEVERYWHERE				---- */

.inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4) {
	background: #fff;
}
.badgesChat-f_cbR8 .inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4),
.badgesList-Aw_p52 .inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4),
.badgesSettings-ychoGn .inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4) {
	background: var(--header-secondary);
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeStaff-3BXdTO {
	-webkit-mask: url(https://discord.com/assets/7cfd90c8062139e4804a1fa59f564731.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgePartner-j6Lwhr {
	-webkit-mask: url(https://discord.com/assets/a0e288a458c48dfcf548dadc277e42e6.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypesquad-12E2P6 {
	-webkit-mask: url(https://discord.com/assets/3a050fcc884255231b99b7033c776070.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse1-3rBtjf {
	-webkit-mask: url(https://discord.com/assets/1115767aed344e96a27a12e97718c171.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse2-2oU04B {
	-webkit-mask: url(https://discord.com/assets/d3478c6bd5cee0fc600e55935ddc81aa.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse3-1DoJkv {
	-webkit-mask: url(https://discord.com/assets/2a085ed9c86f3613935a6a8667ba8b89.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse1Winner-3wCl80 {
	-webkit-mask: url(https://discord.com/assets/75f75c3142b8d44ea7052c2bcb9a9043.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse2Winner-AS5bXe {
	-webkit-mask: url(https://discord.com/assets/d4a8fe68fc5f40c8a778f858881a7b84.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse3Winner-2CwwQi {
	-webkit-mask: url(https://discord.com/assets/5dc48a7859a00e7d95ad8382156aab84.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeEarlySupporter-2ng_jL {
	-webkit-mask: url(https://discord.com/assets/ce15562552e3d70c56d5408cfeed2ffd.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgePremium-1KDZYC {
	-webkit-mask: url(https://discord.com/assets/379d2b3171722ef8be494231234da5d1.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeVerifiedDeveloper-195KfD {
	-webkit-mask: url(https://discord.com/assets/785d81fdbedd133e213da693aba98774.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeBugHunterLevel1-dbEzVz {
	-webkit-mask: url(https://discord.com/assets/df26f079738a4dcd07cbce6eb3c957f1.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeBugHunterLevel2-3TUciC {
	-webkit-mask: url(https://discord.com/assets/16def052b03d75dac0ed9234c5d6a880.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl1-3oI9tx {
	-webkit-mask: url(https://discord.com/assets/24e49184598820f274e62293349a2e43.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl2-r6nJHT {
	-webkit-mask: url(https://discord.com/assets/cc73fba5c2e9b70752bbd1db35a1b9c3.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl3-38s3Dj {
	-webkit-mask: url(https://discord.com/assets/a4c3939a9b03274246df9b144fcd86cf.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl4-2NXrsI {
	-webkit-mask: url(https://discord.com/assets/d01bee8a9b41bd9dda26a43221b2e7e8.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl5-3XIa2K {
	-webkit-mask: url(https://discord.com/assets/a99def5f819c077e5e5061cab741b7e6.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl6-3e3sxW {
	-webkit-mask: url(https://discord.com/assets/2cfb317f3db3963d8ded9a97ee967bac.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl7-1dVhQT {
	-webkit-mask: url(https://discord.com/assets/278736f579d810b11ddf308cb598b19e.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl8-1kXdFr {
	-webkit-mask: url(https://discord.com/assets/38e40f25802a0fdf480d9b855a37a2f3.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl9-1d6zav {
	-webkit-mask: url(https://discord.com/assets/cfbc2d8ceacfacf07850f986c8165195.svg) center/contain no-repeat;
}


/* ~~~~		19.		UPDATENOTICE					~~~~ */

html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp::before {
	content: "Your Version of   BasicBackground   by DevilBro is outdated. Please download the newest Version:	https://mwittrien.github.io/downloader/?theme=BasicBackground" !important;
	display: var(--version1_0_5, block) !important;
	background-color: #4a90e2 !important;
	box-shadow: 0 1px 5px 0 rgba(var(--transparencycolor), .3) !important;
	color: var(--header-primary) !important;
	flex-grow: 0 !important;
	flex-shrink: 0 !important;
	font-size: 14px !important;
	font-weight: 500 !important;
	height: 36px !important;
	line-height: 36px !important;
	opacity: 1 !important;
	padding-left: 4px !important;
	padding-right: 28px !important;
	position: relative !important;
	text-align: center !important;
	visibility: unset !important;
	white-space: pre !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	max-width: unset !important;
	min-width: unset !important;
	max-height: unset !important;
	min-height: unset !important;
	transform: unset !important;
	animation: unset !important;
	z-index: 101 !important;
	pointer-events: none !important;
}


/* ~~~~		20.		WATERMARK						~~~~ */

html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.typeWindows-1za-n7.titleBar-AC4pGV.horizontalReverse-3tRjY7.flex-1O1GKY.directionRowReverse-m8IjIq.justifyStart-2NDFzi.alignStretch-DpGPf3 > div.wordmark-2iDDfm {
	display: block !important;
	color: var(--channels-default) !important;
	position: absolute !important;
	max-width: unset !important;
	min-width: unset !important;
	width: 55px !important;
	max-height: unset !important;
	min-height: unset !important;
	height: 16px !important;
	margin: 0 !important;
	padding: 3px 9px 3px !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.typeWindows-1za-n7.titleBar-AC4pGV.horizontalReverse-3tRjY7.flex-1O1GKY.directionRowReverse-m8IjIq.justifyStart-2NDFzi.alignStretch-DpGPf3 > div.wordmark-2iDDfm > * {
	display: none !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.typeWindows-1za-n7.titleBar-AC4pGV.horizontalReverse-3tRjY7.flex-1O1GKY.directionRowReverse-m8IjIq.justifyStart-2NDFzi.alignStretch-DpGPf3 > div.wordmark-2iDDfm::before {
	content: "" !important;
	background: currentColor !important;
	-webkit-mask: url('data:image/svg+xml; utf8, <svg width="55" height="19" version="1.1" xmlns="http://www.w3.org/2000/svg"><path fill="black" d="M3.57642276,0.141304348 L0,0.141304348 L0,4.22826087 L2.38069106,6.40217391 L2.38069106,2.43478261 L3.66260163,2.43478261 C4.47052846,2.43478261 4.86910569,2.83695652 4.86910569,3.4673913 L4.86910569,6.5 C4.86910569,7.13043478 4.49207317,7.55434783 3.66260163,7.55434783 L0,7.55434783 L0,9.85869565 L3.57642276,9.85869565 C5.49390244,9.86956522 7.29288618,8.90217391 7.29288618,6.66304348 L7.29288618,3.39130435 C7.29288618,1.13043478 5.49390244,0.141304348 3.57642276,0.141304348 Z M22.3310976,6.67391304 L22.3310976,3.32608696 C22.3310976,2.11956522 24.4640244,1.83695652 25.1103659,3.05434783 L27.0817073,2.23913043 C26.3168699,0.510869565 24.8949187,0 23.7207317,0 C21.803252,0 19.9073171,1.13043478 19.9073171,3.32608696 L19.9073171,6.67391304 C19.9073171,8.88043478 21.803252,10 23.6776423,10 C24.8841463,10 26.3276423,9.39130435 27.1247967,7.81521739 L25.0134146,6.82608696 C24.4963415,8.17391304 22.3310976,7.84782609 22.3310976,6.67391304 Z M15.8030488,3.7826087 C15.0597561,3.61956522 14.5642276,3.34782609 14.5319106,2.88043478 C14.575,1.75 16.2878049,1.7173913 17.2896341,2.79347826 L18.8731707,1.55434783 C17.8821138,0.326086957 16.7617886,0 15.598374,0 C13.8424797,0 12.1404472,1 12.1404472,2.91304348 C12.1404472,4.77173913 13.5408537,5.76086957 15.0813008,6 C15.8676829,6.10869565 16.7402439,6.42391304 16.7186992,6.97826087 C16.654065,8.02173913 14.5426829,7.9673913 13.5839431,6.7826087 L12.0650407,8.23913043 C12.9591463,9.40217391 14.1764228,10 15.3182927,10 C17.074187,10 19.0239837,8.9673913 19.0993902,7.08695652 C19.2071138,4.69565217 17.5050813,4.09782609 15.8030488,3.7826087 Z M8.59634146,9.85869565 L11.0093496,9.85869565 L11.0093496,0.141304348 L8.59634146,0.141304348 L8.59634146,9.85869565 Z M49.2835366,0.141304348 L45.7071138,0.141304348 L45.7071138,4.22826087 L48.0878049,6.40217391 L48.0878049,2.43478261 L49.3589431,2.43478261 C50.1668699,2.43478261 50.5654472,2.83695652 50.5654472,3.4673913 L50.5654472,6.5 C50.5654472,7.13043478 50.1884146,7.55434783 49.3589431,7.55434783 L45.6963415,7.55434783 L45.6963415,9.85869565 L49.2727642,9.85869565 C51.1902439,9.86956522 52.9892276,8.90217391 52.9892276,6.66304348 L52.9892276,3.39130435 C53,1.13043478 51.2010163,0.141304348 49.2835366,0.141304348 Z M31.7353659,0 C29.753252,0 27.7819106,1.09782609 27.7819106,3.33695652 L27.7819106,6.66304348 C27.7819106,8.89130435 29.7640244,10 31.7569106,10 C33.7390244,10 35.7103659,8.89130435 35.7103659,6.66304348 L35.7103659,3.33695652 C35.7103659,1.10869565 33.7174797,0 31.7353659,0 Z M33.2865854,6.66304348 C33.2865854,7.35869565 32.5109756,7.7173913 31.7461382,7.7173913 C30.9705285,7.7173913 30.1949187,7.36956522 30.1949187,6.66304348 L30.1949187,3.33695652 C30.1949187,2.61956522 30.9489837,2.23913043 31.7030488,2.23913043 C32.4894309,2.23913043 33.2865854,2.58695652 33.2865854,3.33695652 L33.2865854,6.66304348 Z M44.3605691,3.33695652 C44.3067073,1.05434783 42.7770325,0.141304348 40.8056911,0.141304348 L36.9815041,0.141304348 L36.9815041,9.86956522 L39.4268293,9.86956522 L39.4268293,6.77173913 L39.8577236,6.77173913 L42.0768293,9.85869565 L45.0930894,9.85869565 L42.4861789,6.52173913 C43.6495935,6.15217391 44.3605691,5.14130435 44.3605691,3.33695652 Z M40.8487805,4.65217391 L39.4268293,4.65217391 L39.4268293,2.43478261 L40.8487805,2.43478261 C42.3784553,2.43478261 42.3784553,4.65217391 40.8487805,4.65217391 Z" transform="translate(1 3)"></path></svg>') center/contain no-repeat !important;
	width: 55px !important;
	height: 19px !important;
	display: inline !important;
	position: absolute !important;
	top: unset !important;
	left: unset !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.typeWindows-1za-n7.titleBar-AC4pGV.horizontalReverse-3tRjY7.flex-1O1GKY.directionRowReverse-m8IjIq.justifyStart-2NDFzi.alignStretch-DpGPf3 > div.wordmark-2iDDfm::after {
	content: "" !important;
	background: currentColor !important;
	-webkit-mask: url('data:image/svg+xml; utf8, <svg width="242" height="19" version="1.1" xmlns="http://www.w3.org/2000/svg"><path stroke="none" fill="black" fill-rule="evenodd" transform="scale(0.6, 0.6) translate(5,4)" d="M58.488 0.690 C 54.786 0.948,52.503 3.334,52.961 6.466 C 53.321 8.926,55.135 10.509,58.186 11.025 C 60.205 11.366,61.177 12.097,60.818 13.004 C 60.260 14.412,57.255 14.154,55.679 12.564 L 55.440 12.323 55.340 12.411 C 55.125 12.602,52.767 14.824,52.768 14.836 C 52.768 14.843,52.842 14.938,52.932 15.047 C 55.188 17.761,58.434 18.568,61.663 17.218 C 63.879 16.291,65.049 14.673,65.056 12.523 C 65.066 9.499,63.520 7.999,59.581 7.209 C 57.730 6.838,56.956 6.245,57.139 5.336 C 57.409 3.990,59.424 3.729,61.092 4.823 C 61.328 4.978,61.513 5.126,61.754 5.350 L 61.902 5.489 63.269 4.436 C 64.021 3.857,64.640 3.372,64.645 3.357 C 64.668 3.286,63.905 2.499,63.488 2.164 C 62.141 1.082,60.367 0.559,58.488 0.690 M79.453 0.691 C 76.162 0.865,73.785 2.780,73.354 5.604 C 73.306 5.919,73.281 11.980,73.325 12.570 C 73.506 14.979,75.020 16.759,77.535 17.519 C 80.709 18.479,83.881 17.374,85.557 14.725 C 85.782 14.369,85.916 14.116,85.893 14.093 C 85.872 14.073,82.327 12.430,82.254 12.406 C 82.224 12.397,82.198 12.429,82.144 12.544 C 81.882 13.103,81.353 13.555,80.730 13.752 C 79.382 14.177,77.866 13.572,77.593 12.501 C 77.539 12.288,77.540 6.228,77.595 6.015 C 78.042 4.261,81.252 4.104,82.289 5.785 C 82.338 5.865,82.385 5.930,82.393 5.930 C 82.409 5.930,85.820 4.554,85.837 4.541 C 85.856 4.526,85.497 3.838,85.340 3.588 C 84.071 1.573,82.003 0.555,79.453 0.691 M122.233 0.698 C 118.928 0.954,116.621 2.860,116.252 5.640 C 116.198 6.046,116.207 12.646,116.263 13.000 C 116.678 15.665,118.768 17.446,121.919 17.818 C 124.720 18.149,127.505 16.687,128.743 14.235 L 128.815 14.092 128.669 14.026 C 128.589 13.989,127.762 13.608,126.832 13.177 C 125.902 12.747,125.135 12.395,125.129 12.395 C 125.122 12.395,125.079 12.471,125.032 12.564 C 124.149 14.321,121.136 14.341,120.519 12.593 L 120.453 12.407 120.447 9.350 C 120.442 6.713,120.445 6.267,120.476 6.106 C 120.814 4.288,124.035 4.054,125.172 5.764 C 125.233 5.855,125.288 5.930,125.294 5.930 C 125.318 5.930,128.710 4.554,128.727 4.537 C 128.750 4.515,128.506 4.030,128.302 3.691 C 127.042 1.592,124.822 0.498,122.233 0.698 M150.163 0.690 C 146.674 0.881,144.259 2.928,144.024 5.893 C 143.992 6.292,143.992 12.111,144.024 12.535 C 144.229 15.291,146.239 17.273,149.317 17.756 C 152.815 18.304,156.021 16.678,156.902 13.907 C 157.157 13.104,157.167 12.980,157.179 10.250 L 157.190 7.907 153.816 7.907 L 150.442 7.907 150.442 9.686 L 150.442 11.465 151.770 11.465 L 153.098 11.465 153.088 11.948 C 153.069 12.840,152.771 13.335,152.028 13.707 C 150.559 14.443,148.672 13.843,148.297 12.522 L 148.244 12.337 148.244 9.221 L 148.244 6.105 148.296 5.922 C 148.641 4.708,150.215 4.096,151.595 4.640 C 152.111 4.844,152.607 5.305,152.816 5.777 C 152.852 5.859,152.875 5.885,152.903 5.877 C 152.970 5.857,156.383 4.277,156.404 4.256 C 156.456 4.205,156.028 3.438,155.709 3.012 C 154.517 1.418,152.475 0.563,150.163 0.690 M180.081 0.700 C 176.707 0.925,174.383 2.695,173.857 5.442 C 173.796 5.758,173.758 12.153,173.814 12.721 C 174.112 15.773,176.906 17.847,180.721 17.847 C 184.496 17.847,187.238 15.831,187.594 12.794 C 187.645 12.357,187.645 6.177,187.593 5.740 C 187.221 2.553,184.063 0.434,180.081 0.700 M390.026 0.701 C 386.623 0.917,384.214 2.823,383.799 5.628 C 383.750 5.958,383.722 11.716,383.765 12.444 C 383.954 15.593,386.593 17.735,390.430 17.853 C 394.202 17.969,397.090 15.976,397.551 12.938 C 397.616 12.508,397.615 6.017,397.550 5.593 C 397.065 2.452,393.986 0.450,390.026 0.701 M249.326 4.333 C 249.326 7.601,249.328 7.786,249.366 7.797 C 249.389 7.803,250.338 8.626,251.477 9.625 C 252.615 10.624,253.554 11.442,253.564 11.442 C 253.574 11.442,253.581 9.871,253.581 7.952 L 253.581 4.462 254.948 4.471 C 256.262 4.479,256.321 4.481,256.495 4.530 C 257.918 4.924,257.953 6.870,256.547 7.343 L 256.360 7.405 255.366 7.414 L 254.372 7.422 254.372 8.954 L 254.372 10.486 255.413 10.494 C 256.589 10.503,256.592 10.504,257.000 10.704 C 258.198 11.291,258.196 13.081,256.998 13.659 C 256.517 13.891,256.654 13.884,252.716 13.884 L 249.326 13.884 249.326 15.744 L 249.326 17.605 252.831 17.604 C 256.414 17.604,256.877 17.595,257.522 17.512 C 260.168 17.172,261.703 15.747,262.103 13.259 C 262.394 11.447,261.566 9.707,259.993 8.829 C 259.761 8.699,259.762 8.700,259.877 8.639 C 260.813 8.141,261.456 6.960,261.452 5.744 C 261.445 3.299,259.914 1.508,257.419 1.024 C 256.765 0.897,256.875 0.901,252.959 0.890 L 249.326 0.881 249.326 4.333 M317.842 0.913 C 317.848 0.929,319.202 4.691,320.851 9.273 L 323.849 17.604 325.791 17.604 L 327.733 17.605 330.739 9.259 C 332.392 4.669,333.744 0.907,333.744 0.899 C 333.744 0.891,332.721 0.884,331.471 0.884 L 329.198 0.884 327.877 4.983 L 326.556 9.081 326.185 11.012 C 325.982 12.073,325.815 12.955,325.814 12.971 C 325.814 12.987,325.801 13.000,325.785 13.000 C 325.765 13.000,325.639 12.389,325.380 11.025 L 325.004 9.049 323.695 4.966 L 322.385 0.884 320.109 0.884 C 318.298 0.884,317.834 0.890,317.842 0.913 M354.349 4.333 C 354.349 7.601,354.351 7.786,354.390 7.797 C 354.412 7.803,355.362 8.626,356.500 9.625 C 357.638 10.624,358.578 11.442,358.587 11.442 C 358.597 11.442,358.605 9.871,358.605 7.952 L 358.605 4.462 359.971 4.471 C 361.286 4.479,361.344 4.481,361.519 4.530 C 362.941 4.924,362.976 6.870,361.570 7.343 L 361.384 7.405 360.390 7.414 L 359.395 7.422 359.395 8.954 L 359.395 10.486 360.436 10.494 C 361.613 10.503,361.615 10.504,362.023 10.704 C 363.221 11.291,363.220 13.081,362.021 13.659 C 361.541 13.891,361.678 13.884,357.739 13.884 L 354.349 13.884 354.349 15.744 L 354.349 17.605 357.855 17.604 C 361.438 17.604,361.900 17.595,362.546 17.512 C 365.191 17.172,366.726 15.747,367.126 13.259 C 367.418 11.447,366.589 9.707,365.017 8.829 C 364.784 8.699,364.785 8.700,364.900 8.639 C 365.836 8.141,366.479 6.960,366.475 5.744 C 366.468 3.299,364.938 1.508,362.442 1.024 C 361.788 0.897,361.898 0.901,357.983 0.890 L 354.349 0.881 354.349 4.333 M24.186 4.356 C 24.186 7.624,24.188 7.809,24.227 7.820 C 24.249 7.827,25.199 8.649,26.337 9.648 C 27.476 10.647,28.415 11.465,28.424 11.465 C 28.434 11.465,28.442 9.895,28.442 7.975 L 28.442 4.485 29.808 4.494 C 31.123 4.502,31.181 4.505,31.356 4.553 C 32.778 4.947,32.813 6.893,31.407 7.366 L 31.221 7.429 30.227 7.437 L 29.233 7.445 29.233 8.977 L 29.233 10.509 30.273 10.517 C 31.450 10.527,31.452 10.527,31.860 10.727 C 33.058 11.314,33.057 13.104,31.858 13.682 C 31.378 13.914,31.515 13.907,27.576 13.907 L 24.186 13.907 24.186 15.767 L 24.186 17.628 27.692 17.627 C 31.275 17.627,31.737 17.618,32.383 17.535 C 35.028 17.195,36.564 15.770,36.964 13.282 C 37.255 11.471,36.426 9.731,34.854 8.852 C 34.621 8.722,34.622 8.724,34.738 8.662 C 35.674 8.165,36.316 6.984,36.312 5.767 C 36.305 3.322,34.775 1.531,32.279 1.047 C 31.625 0.921,31.735 0.924,27.820 0.914 L 24.186 0.904 24.186 4.356 M42.922 0.925 C 42.916 0.934,41.608 4.678,40.015 9.244 C 38.423 13.811,37.113 17.565,37.104 17.587 C 37.089 17.626,37.206 17.628,39.368 17.628 C 41.519 17.628,41.649 17.626,41.660 17.587 C 41.667 17.565,41.898 16.817,42.173 15.925 C 42.449 15.034,42.674 14.298,42.674 14.292 C 42.674 14.285,43.673 14.279,44.894 14.279 L 47.114 14.279 47.346 14.994 C 47.474 15.388,47.718 16.141,47.888 16.669 L 48.198 17.628 50.473 17.628 C 52.284 17.628,52.747 17.622,52.739 17.599 C 52.734 17.583,51.390 13.821,49.754 9.238 L 46.779 0.907 44.856 0.907 C 43.798 0.907,42.928 0.915,42.922 0.925 M66.860 9.267 L 66.860 17.628 68.977 17.628 L 71.093 17.628 71.093 9.267 L 71.093 0.907 68.977 0.907 L 66.860 0.907 66.860 9.267 M103.247 9.239 C 101.649 13.821,100.337 17.583,100.331 17.599 C 100.323 17.622,100.786 17.628,102.598 17.628 L 104.875 17.628 105.348 16.099 C 105.609 15.258,105.841 14.504,105.865 14.424 L 105.909 14.279 108.128 14.279 L 110.346 14.279 110.448 14.599 C 110.504 14.775,110.747 15.528,110.989 16.273 L 111.427 17.628 113.704 17.628 C 115.516 17.628,115.980 17.622,115.971 17.599 C 115.965 17.583,114.622 13.821,112.986 9.239 L 110.012 0.908 108.081 0.908 L 106.151 0.908 103.247 9.239 M130.326 9.267 L 130.326 17.628 132.453 17.628 L 134.581 17.628 134.581 14.740 L 134.581 11.851 134.644 11.761 C 134.696 11.686,134.711 11.676,134.731 11.705 C 134.745 11.723,135.703 13.064,136.860 14.683 L 138.965 17.627 141.648 17.627 C 144.025 17.628,144.329 17.624,144.317 17.593 C 144.308 17.568,137.994 9.268,137.789 9.011 C 137.778 8.996,139.071 7.397,141.060 4.969 C 142.869 2.759,144.349 0.941,144.349 0.929 C 144.349 0.915,143.342 0.907,141.715 0.908 L 139.081 0.909 136.837 3.975 L 134.593 7.041 134.587 3.974 L 134.581 0.907 132.453 0.907 L 130.326 0.907 130.326 9.267 M159.116 9.266 L 159.116 17.628 161.256 17.628 L 163.395 17.628 163.395 14.977 L 163.395 12.326 163.762 12.326 L 164.129 12.326 166.058 14.976 L 167.988 17.626 170.625 17.627 C 172.875 17.628,173.259 17.623,173.248 17.595 C 173.241 17.577,172.224 16.288,170.987 14.730 C 169.750 13.172,168.747 11.894,168.759 11.890 C 170.569 11.276,171.641 9.837,171.917 7.651 C 172.346 4.246,170.890 1.873,167.930 1.154 C 166.981 0.924,166.973 0.924,162.785 0.913 L 159.116 0.904 159.116 9.266 M189.767 6.704 C 189.767 12.984,189.763 12.742,189.893 13.354 C 190.564 16.526,194.059 18.450,197.907 17.766 C 200.535 17.299,202.429 15.647,202.943 13.372 C 203.088 12.729,203.079 13.167,203.087 6.750 L 203.094 0.907 200.955 0.907 L 198.815 0.907 198.808 6.599 C 198.801 11.986,198.798 12.299,198.759 12.453 C 198.236 14.492,194.735 14.570,194.112 12.558 L 194.058 12.384 194.052 6.645 L 194.046 0.907 191.907 0.907 L 189.767 0.907 189.767 6.704 M205.558 9.267 L 205.558 17.628 207.674 17.628 L 209.791 17.628 209.790 14.238 L 209.790 10.849 209.526 9.285 C 209.175 7.205,209.135 7.199,210.080 9.366 L 210.797 11.012 212.694 14.320 L 214.591 17.628 216.726 17.628 L 218.860 17.628 218.860 9.267 L 218.860 0.907 216.756 0.907 L 214.651 0.907 214.651 4.682 C 214.651 7.186,214.659 8.500,214.675 8.587 C 214.747 8.973,215.111 11.338,215.102 11.354 C 215.060 11.421,214.969 11.226,214.320 9.692 L 213.610 8.012 211.600 4.465 L 209.590 0.919 207.574 0.913 L 205.558 0.907 205.558 9.267 M221.488 4.334 C 221.488 7.579,221.491 7.763,221.529 7.774 C 221.551 7.780,222.501 8.603,223.640 9.602 C 224.778 10.601,225.717 11.418,225.727 11.418 C 225.736 11.419,225.744 9.948,225.744 8.150 L 225.744 4.881 227.087 4.889 L 228.430 4.897 228.663 4.960 C 229.357 5.146,229.767 5.539,229.922 6.163 C 229.963 6.328,229.965 6.490,229.965 9.244 L 229.965 12.151 229.913 12.349 C 229.704 13.139,229.110 13.560,228.105 13.628 C 227.923 13.641,226.390 13.651,224.634 13.651 L 221.488 13.651 221.488 15.640 L 221.488 17.628 224.738 17.628 C 228.530 17.628,228.747 17.619,229.628 17.442 C 232.189 16.927,233.789 15.382,234.170 13.058 C 234.229 12.694,234.263 6.624,234.209 5.965 C 233.966 2.989,231.727 1.114,228.198 0.930 C 227.951 0.918,226.369 0.907,224.622 0.907 L 221.488 0.907 221.488 4.334 M261.518 0.936 C 261.525 0.952,262.834 3.230,264.428 5.997 L 267.326 11.030 267.326 14.329 L 267.326 17.628 269.453 17.628 L 271.581 17.628 271.581 14.331 L 271.581 11.034 274.491 6.000 C 276.091 3.232,277.406 0.953,277.412 0.937 C 277.421 0.913,276.956 0.907,274.937 0.907 L 272.450 0.907 270.952 3.953 C 270.128 5.629,269.448 7.000,269.442 6.999 C 269.435 6.999,268.756 5.628,267.932 3.953 L 266.435 0.907 263.971 0.907 C 262.009 0.907,261.509 0.913,261.518 0.936 M290.535 4.334 C 290.535 7.579,290.537 7.763,290.576 7.774 C 290.598 7.780,291.548 8.603,292.686 9.602 C 293.824 10.601,294.764 11.418,294.773 11.418 C 294.783 11.419,294.791 9.948,294.791 8.150 L 294.791 4.881 296.134 4.889 L 297.477 4.897 297.709 4.960 C 298.403 5.146,298.814 5.539,298.968 6.163 C 299.009 6.328,299.012 6.490,299.012 9.244 L 299.012 12.151 298.959 12.349 C 298.751 13.139,298.157 13.560,297.151 13.628 C 296.970 13.641,295.436 13.651,293.680 13.651 L 290.535 13.651 290.535 15.640 L 290.535 17.628 293.785 17.628 C 297.577 17.628,297.794 17.619,298.674 17.442 C 301.235 16.927,302.836 15.382,303.216 13.058 C 303.276 12.694,303.310 6.624,303.256 5.965 C 303.013 2.989,300.774 1.114,297.244 0.930 C 296.998 0.918,295.416 0.907,293.669 0.907 L 290.535 0.907 290.535 4.334 M305.512 9.267 L 305.512 17.628 311.337 17.628 L 317.163 17.628 317.163 15.616 L 317.163 13.605 313.488 13.605 L 309.814 13.605 309.814 12.372 L 309.814 11.140 313.186 11.140 L 316.558 11.140 316.558 9.302 L 316.558 7.465 313.186 7.465 L 309.814 7.465 309.814 6.186 L 309.814 4.907 313.488 4.907 L 317.163 4.907 317.163 2.907 L 317.163 0.907 311.337 0.907 L 305.512 0.907 305.512 9.267 M334.814 9.267 L 334.814 17.628 336.942 17.628 L 339.070 17.628 339.070 9.267 L 339.070 0.907 336.942 0.907 L 334.814 0.907 334.814 9.267 M341.674 9.267 L 341.674 17.628 347.198 17.628 L 352.721 17.628 352.721 15.523 L 352.721 13.419 349.326 13.419 L 345.930 13.419 345.930 7.163 L 345.930 0.907 343.802 0.907 L 341.674 0.907 341.674 9.267 M369.070 9.267 L 369.070 17.628 371.221 17.628 L 373.372 17.628 373.372 14.977 L 373.372 12.326 373.738 12.327 L 374.105 12.328 376.034 14.978 L 377.963 17.628 380.598 17.628 C 382.047 17.628,383.232 17.620,383.232 17.610 C 383.232 17.601,382.367 16.505,381.311 15.174 C 380.254 13.844,379.235 12.561,379.047 12.324 L 378.704 11.891 378.916 11.815 C 380.927 11.094,382.015 9.124,381.947 6.327 C 381.871 3.234,380.093 1.352,376.892 0.978 C 376.397 0.920,375.607 0.908,372.424 0.907 L 369.070 0.907 369.070 9.267 M87.395 4.380 C 87.395 7.647,87.398 7.832,87.436 7.843 C 87.458 7.850,88.408 8.672,89.547 9.672 C 90.685 10.671,91.624 11.488,91.634 11.488 C 91.643 11.488,91.651 9.918,91.651 7.998 L 91.651 4.508 93.017 4.517 C 94.332 4.526,94.391 4.528,94.565 4.576 C 95.987 4.971,96.023 6.916,94.616 7.389 L 94.430 7.452 93.436 7.460 L 92.442 7.468 92.442 9.000 L 92.442 10.532 93.483 10.541 C 94.659 10.550,94.662 10.550,95.070 10.750 C 96.268 11.337,96.266 13.127,95.067 13.706 C 94.587 13.937,94.724 13.930,90.785 13.930 L 87.395 13.930 87.395 15.791 L 87.395 17.651 90.901 17.651 C 94.484 17.650,94.947 17.641,95.592 17.558 C 98.238 17.219,99.773 15.793,100.173 13.306 C 100.464 11.494,99.636 9.754,98.063 8.875 C 97.831 8.745,97.832 8.747,97.947 8.686 C 98.883 8.188,99.526 7.007,99.522 5.791 C 99.514 3.345,97.984 1.554,95.488 1.071 C 94.834 0.944,94.944 0.947,91.029 0.937 L 87.395 0.927 87.395 4.380 M181.387 4.605 C 182.483 4.791,183.204 5.337,183.359 6.098 C 183.414 6.371,183.414 12.174,183.358 12.426 C 182.924 14.391,178.570 14.432,178.069 12.475 C 178.004 12.220,177.997 6.370,178.061 6.086 C 178.311 4.984,179.776 4.331,181.387 4.605 M391.352 4.603 C 392.415 4.786,393.110 5.288,393.318 6.023 C 393.384 6.258,393.384 12.254,393.318 12.488 C 392.775 14.411,388.490 14.392,388.036 12.464 C 387.983 12.238,387.982 6.267,388.035 6.057 C 388.309 4.975,389.775 4.332,391.352 4.603 M166.461 4.949 C 168.323 5.517,168.296 8.092,166.423 8.599 L 166.198 8.660 164.797 8.669 L 163.395 8.678 163.395 6.780 L 163.395 4.881 164.843 4.889 C 166.263 4.897,166.294 4.898,166.461 4.949 M376.423 4.947 C 378.081 5.414,378.313 7.706,376.779 8.453 C 376.357 8.659,376.206 8.674,374.634 8.674 L 373.372 8.674 373.372 6.778 L 373.372 4.882 374.808 4.889 C 376.199 4.896,376.250 4.898,376.423 4.947 M44.953 5.669 C 44.953 5.679,45.210 6.770,45.523 8.093 C 45.837 9.416,46.093 10.501,46.093 10.505 C 46.093 10.509,45.538 10.512,44.859 10.512 C 43.881 10.512,43.626 10.506,43.635 10.483 C 43.641 10.467,43.916 9.373,44.247 8.052 C 44.823 5.756,44.851 5.651,44.901 5.651 C 44.930 5.651,44.953 5.659,44.953 5.669 M108.742 8.052 C 109.054 9.373,109.314 10.467,109.320 10.483 C 109.328 10.506,109.073 10.512,108.093 10.512 C 107.113 10.512,106.858 10.506,106.865 10.483 C 106.871 10.467,107.147 9.373,107.478 8.052 C 108.029 5.862,108.085 5.651,108.128 5.651 C 108.171 5.651,108.222 5.849,108.742 8.052 M5.419 9.453 L 5.419 11.465 9.105 11.465 L 12.791 11.465 12.791 9.453 L 12.791 7.442 9.105 7.442 L 5.419 7.442 5.419 9.453"></path></svg>') center/contain no-repeat !important;
	width: 242px !important;
	height: 19px !important;
	display: inline !important;
	position: absolute !important;
	top: unset !important;
	left: 64px !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}

html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i::after {
	content: url('data:image/svg+xml; utf8, <svg width="400" height="18" version="1.1" xmlns="http://www.w3.org/2000/svg"><path stroke="none" fill="rgb(255, 255, 255)" fill-rule="evenodd" d="M58.488 0.690 C 54.786 0.948,52.503 3.334,52.961 6.466 C 53.321 8.926,55.135 10.509,58.186 11.025 C 60.205 11.366,61.177 12.097,60.818 13.004 C 60.260 14.412,57.255 14.154,55.679 12.564 L 55.440 12.323 55.340 12.411 C 55.125 12.602,52.767 14.824,52.768 14.836 C 52.768 14.843,52.842 14.938,52.932 15.047 C 55.188 17.761,58.434 18.568,61.663 17.218 C 63.879 16.291,65.049 14.673,65.056 12.523 C 65.066 9.499,63.520 7.999,59.581 7.209 C 57.730 6.838,56.956 6.245,57.139 5.336 C 57.409 3.990,59.424 3.729,61.092 4.823 C 61.328 4.978,61.513 5.126,61.754 5.350 L 61.902 5.489 63.269 4.436 C 64.021 3.857,64.640 3.372,64.645 3.357 C 64.668 3.286,63.905 2.499,63.488 2.164 C 62.141 1.082,60.367 0.559,58.488 0.690 M79.453 0.691 C 76.162 0.865,73.785 2.780,73.354 5.604 C 73.306 5.919,73.281 11.980,73.325 12.570 C 73.506 14.979,75.020 16.759,77.535 17.519 C 80.709 18.479,83.881 17.374,85.557 14.725 C 85.782 14.369,85.916 14.116,85.893 14.093 C 85.872 14.073,82.327 12.430,82.254 12.406 C 82.224 12.397,82.198 12.429,82.144 12.544 C 81.882 13.103,81.353 13.555,80.730 13.752 C 79.382 14.177,77.866 13.572,77.593 12.501 C 77.539 12.288,77.540 6.228,77.595 6.015 C 78.042 4.261,81.252 4.104,82.289 5.785 C 82.338 5.865,82.385 5.930,82.393 5.930 C 82.409 5.930,85.820 4.554,85.837 4.541 C 85.856 4.526,85.497 3.838,85.340 3.588 C 84.071 1.573,82.003 0.555,79.453 0.691 M122.233 0.698 C 118.928 0.954,116.621 2.860,116.252 5.640 C 116.198 6.046,116.207 12.646,116.263 13.000 C 116.678 15.665,118.768 17.446,121.919 17.818 C 124.720 18.149,127.505 16.687,128.743 14.235 L 128.815 14.092 128.669 14.026 C 128.589 13.989,127.762 13.608,126.832 13.177 C 125.902 12.747,125.135 12.395,125.129 12.395 C 125.122 12.395,125.079 12.471,125.032 12.564 C 124.149 14.321,121.136 14.341,120.519 12.593 L 120.453 12.407 120.447 9.350 C 120.442 6.713,120.445 6.267,120.476 6.106 C 120.814 4.288,124.035 4.054,125.172 5.764 C 125.233 5.855,125.288 5.930,125.294 5.930 C 125.318 5.930,128.710 4.554,128.727 4.537 C 128.750 4.515,128.506 4.030,128.302 3.691 C 127.042 1.592,124.822 0.498,122.233 0.698 M150.163 0.690 C 146.674 0.881,144.259 2.928,144.024 5.893 C 143.992 6.292,143.992 12.111,144.024 12.535 C 144.229 15.291,146.239 17.273,149.317 17.756 C 152.815 18.304,156.021 16.678,156.902 13.907 C 157.157 13.104,157.167 12.980,157.179 10.250 L 157.190 7.907 153.816 7.907 L 150.442 7.907 150.442 9.686 L 150.442 11.465 151.770 11.465 L 153.098 11.465 153.088 11.948 C 153.069 12.840,152.771 13.335,152.028 13.707 C 150.559 14.443,148.672 13.843,148.297 12.522 L 148.244 12.337 148.244 9.221 L 148.244 6.105 148.296 5.922 C 148.641 4.708,150.215 4.096,151.595 4.640 C 152.111 4.844,152.607 5.305,152.816 5.777 C 152.852 5.859,152.875 5.885,152.903 5.877 C 152.970 5.857,156.383 4.277,156.404 4.256 C 156.456 4.205,156.028 3.438,155.709 3.012 C 154.517 1.418,152.475 0.563,150.163 0.690 M180.081 0.700 C 176.707 0.925,174.383 2.695,173.857 5.442 C 173.796 5.758,173.758 12.153,173.814 12.721 C 174.112 15.773,176.906 17.847,180.721 17.847 C 184.496 17.847,187.238 15.831,187.594 12.794 C 187.645 12.357,187.645 6.177,187.593 5.740 C 187.221 2.553,184.063 0.434,180.081 0.700 M390.026 0.701 C 386.623 0.917,384.214 2.823,383.799 5.628 C 383.750 5.958,383.722 11.716,383.765 12.444 C 383.954 15.593,386.593 17.735,390.430 17.853 C 394.202 17.969,397.090 15.976,397.551 12.938 C 397.616 12.508,397.615 6.017,397.550 5.593 C 397.065 2.452,393.986 0.450,390.026 0.701 M249.326 4.333 C 249.326 7.601,249.328 7.786,249.366 7.797 C 249.389 7.803,250.338 8.626,251.477 9.625 C 252.615 10.624,253.554 11.442,253.564 11.442 C 253.574 11.442,253.581 9.871,253.581 7.952 L 253.581 4.462 254.948 4.471 C 256.262 4.479,256.321 4.481,256.495 4.530 C 257.918 4.924,257.953 6.870,256.547 7.343 L 256.360 7.405 255.366 7.414 L 254.372 7.422 254.372 8.954 L 254.372 10.486 255.413 10.494 C 256.589 10.503,256.592 10.504,257.000 10.704 C 258.198 11.291,258.196 13.081,256.998 13.659 C 256.517 13.891,256.654 13.884,252.716 13.884 L 249.326 13.884 249.326 15.744 L 249.326 17.605 252.831 17.604 C 256.414 17.604,256.877 17.595,257.522 17.512 C 260.168 17.172,261.703 15.747,262.103 13.259 C 262.394 11.447,261.566 9.707,259.993 8.829 C 259.761 8.699,259.762 8.700,259.877 8.639 C 260.813 8.141,261.456 6.960,261.452 5.744 C 261.445 3.299,259.914 1.508,257.419 1.024 C 256.765 0.897,256.875 0.901,252.959 0.890 L 249.326 0.881 249.326 4.333 M317.842 0.913 C 317.848 0.929,319.202 4.691,320.851 9.273 L 323.849 17.604 325.791 17.604 L 327.733 17.605 330.739 9.259 C 332.392 4.669,333.744 0.907,333.744 0.899 C 333.744 0.891,332.721 0.884,331.471 0.884 L 329.198 0.884 327.877 4.983 L 326.556 9.081 326.185 11.012 C 325.982 12.073,325.815 12.955,325.814 12.971 C 325.814 12.987,325.801 13.000,325.785 13.000 C 325.765 13.000,325.639 12.389,325.380 11.025 L 325.004 9.049 323.695 4.966 L 322.385 0.884 320.109 0.884 C 318.298 0.884,317.834 0.890,317.842 0.913 M354.349 4.333 C 354.349 7.601,354.351 7.786,354.390 7.797 C 354.412 7.803,355.362 8.626,356.500 9.625 C 357.638 10.624,358.578 11.442,358.587 11.442 C 358.597 11.442,358.605 9.871,358.605 7.952 L 358.605 4.462 359.971 4.471 C 361.286 4.479,361.344 4.481,361.519 4.530 C 362.941 4.924,362.976 6.870,361.570 7.343 L 361.384 7.405 360.390 7.414 L 359.395 7.422 359.395 8.954 L 359.395 10.486 360.436 10.494 C 361.613 10.503,361.615 10.504,362.023 10.704 C 363.221 11.291,363.220 13.081,362.021 13.659 C 361.541 13.891,361.678 13.884,357.739 13.884 L 354.349 13.884 354.349 15.744 L 354.349 17.605 357.855 17.604 C 361.438 17.604,361.900 17.595,362.546 17.512 C 365.191 17.172,366.726 15.747,367.126 13.259 C 367.418 11.447,366.589 9.707,365.017 8.829 C 364.784 8.699,364.785 8.700,364.900 8.639 C 365.836 8.141,366.479 6.960,366.475 5.744 C 366.468 3.299,364.938 1.508,362.442 1.024 C 361.788 0.897,361.898 0.901,357.983 0.890 L 354.349 0.881 354.349 4.333 M24.186 4.356 C 24.186 7.624,24.188 7.809,24.227 7.820 C 24.249 7.827,25.199 8.649,26.337 9.648 C 27.476 10.647,28.415 11.465,28.424 11.465 C 28.434 11.465,28.442 9.895,28.442 7.975 L 28.442 4.485 29.808 4.494 C 31.123 4.502,31.181 4.505,31.356 4.553 C 32.778 4.947,32.813 6.893,31.407 7.366 L 31.221 7.429 30.227 7.437 L 29.233 7.445 29.233 8.977 L 29.233 10.509 30.273 10.517 C 31.450 10.527,31.452 10.527,31.860 10.727 C 33.058 11.314,33.057 13.104,31.858 13.682 C 31.378 13.914,31.515 13.907,27.576 13.907 L 24.186 13.907 24.186 15.767 L 24.186 17.628 27.692 17.627 C 31.275 17.627,31.737 17.618,32.383 17.535 C 35.028 17.195,36.564 15.770,36.964 13.282 C 37.255 11.471,36.426 9.731,34.854 8.852 C 34.621 8.722,34.622 8.724,34.738 8.662 C 35.674 8.165,36.316 6.984,36.312 5.767 C 36.305 3.322,34.775 1.531,32.279 1.047 C 31.625 0.921,31.735 0.924,27.820 0.914 L 24.186 0.904 24.186 4.356 M42.922 0.925 C 42.916 0.934,41.608 4.678,40.015 9.244 C 38.423 13.811,37.113 17.565,37.104 17.587 C 37.089 17.626,37.206 17.628,39.368 17.628 C 41.519 17.628,41.649 17.626,41.660 17.587 C 41.667 17.565,41.898 16.817,42.173 15.925 C 42.449 15.034,42.674 14.298,42.674 14.292 C 42.674 14.285,43.673 14.279,44.894 14.279 L 47.114 14.279 47.346 14.994 C 47.474 15.388,47.718 16.141,47.888 16.669 L 48.198 17.628 50.473 17.628 C 52.284 17.628,52.747 17.622,52.739 17.599 C 52.734 17.583,51.390 13.821,49.754 9.238 L 46.779 0.907 44.856 0.907 C 43.798 0.907,42.928 0.915,42.922 0.925 M66.860 9.267 L 66.860 17.628 68.977 17.628 L 71.093 17.628 71.093 9.267 L 71.093 0.907 68.977 0.907 L 66.860 0.907 66.860 9.267 M103.247 9.239 C 101.649 13.821,100.337 17.583,100.331 17.599 C 100.323 17.622,100.786 17.628,102.598 17.628 L 104.875 17.628 105.348 16.099 C 105.609 15.258,105.841 14.504,105.865 14.424 L 105.909 14.279 108.128 14.279 L 110.346 14.279 110.448 14.599 C 110.504 14.775,110.747 15.528,110.989 16.273 L 111.427 17.628 113.704 17.628 C 115.516 17.628,115.980 17.622,115.971 17.599 C 115.965 17.583,114.622 13.821,112.986 9.239 L 110.012 0.908 108.081 0.908 L 106.151 0.908 103.247 9.239 M130.326 9.267 L 130.326 17.628 132.453 17.628 L 134.581 17.628 134.581 14.740 L 134.581 11.851 134.644 11.761 C 134.696 11.686,134.711 11.676,134.731 11.705 C 134.745 11.723,135.703 13.064,136.860 14.683 L 138.965 17.627 141.648 17.627 C 144.025 17.628,144.329 17.624,144.317 17.593 C 144.308 17.568,137.994 9.268,137.789 9.011 C 137.778 8.996,139.071 7.397,141.060 4.969 C 142.869 2.759,144.349 0.941,144.349 0.929 C 144.349 0.915,143.342 0.907,141.715 0.908 L 139.081 0.909 136.837 3.975 L 134.593 7.041 134.587 3.974 L 134.581 0.907 132.453 0.907 L 130.326 0.907 130.326 9.267 M159.116 9.266 L 159.116 17.628 161.256 17.628 L 163.395 17.628 163.395 14.977 L 163.395 12.326 163.762 12.326 L 164.129 12.326 166.058 14.976 L 167.988 17.626 170.625 17.627 C 172.875 17.628,173.259 17.623,173.248 17.595 C 173.241 17.577,172.224 16.288,170.987 14.730 C 169.750 13.172,168.747 11.894,168.759 11.890 C 170.569 11.276,171.641 9.837,171.917 7.651 C 172.346 4.246,170.890 1.873,167.930 1.154 C 166.981 0.924,166.973 0.924,162.785 0.913 L 159.116 0.904 159.116 9.266 M189.767 6.704 C 189.767 12.984,189.763 12.742,189.893 13.354 C 190.564 16.526,194.059 18.450,197.907 17.766 C 200.535 17.299,202.429 15.647,202.943 13.372 C 203.088 12.729,203.079 13.167,203.087 6.750 L 203.094 0.907 200.955 0.907 L 198.815 0.907 198.808 6.599 C 198.801 11.986,198.798 12.299,198.759 12.453 C 198.236 14.492,194.735 14.570,194.112 12.558 L 194.058 12.384 194.052 6.645 L 194.046 0.907 191.907 0.907 L 189.767 0.907 189.767 6.704 M205.558 9.267 L 205.558 17.628 207.674 17.628 L 209.791 17.628 209.790 14.238 L 209.790 10.849 209.526 9.285 C 209.175 7.205,209.135 7.199,210.080 9.366 L 210.797 11.012 212.694 14.320 L 214.591 17.628 216.726 17.628 L 218.860 17.628 218.860 9.267 L 218.860 0.907 216.756 0.907 L 214.651 0.907 214.651 4.682 C 214.651 7.186,214.659 8.500,214.675 8.587 C 214.747 8.973,215.111 11.338,215.102 11.354 C 215.060 11.421,214.969 11.226,214.320 9.692 L 213.610 8.012 211.600 4.465 L 209.590 0.919 207.574 0.913 L 205.558 0.907 205.558 9.267 M221.488 4.334 C 221.488 7.579,221.491 7.763,221.529 7.774 C 221.551 7.780,222.501 8.603,223.640 9.602 C 224.778 10.601,225.717 11.418,225.727 11.418 C 225.736 11.419,225.744 9.948,225.744 8.150 L 225.744 4.881 227.087 4.889 L 228.430 4.897 228.663 4.960 C 229.357 5.146,229.767 5.539,229.922 6.163 C 229.963 6.328,229.965 6.490,229.965 9.244 L 229.965 12.151 229.913 12.349 C 229.704 13.139,229.110 13.560,228.105 13.628 C 227.923 13.641,226.390 13.651,224.634 13.651 L 221.488 13.651 221.488 15.640 L 221.488 17.628 224.738 17.628 C 228.530 17.628,228.747 17.619,229.628 17.442 C 232.189 16.927,233.789 15.382,234.170 13.058 C 234.229 12.694,234.263 6.624,234.209 5.965 C 233.966 2.989,231.727 1.114,228.198 0.930 C 227.951 0.918,226.369 0.907,224.622 0.907 L 221.488 0.907 221.488 4.334 M261.518 0.936 C 261.525 0.952,262.834 3.230,264.428 5.997 L 267.326 11.030 267.326 14.329 L 267.326 17.628 269.453 17.628 L 271.581 17.628 271.581 14.331 L 271.581 11.034 274.491 6.000 C 276.091 3.232,277.406 0.953,277.412 0.937 C 277.421 0.913,276.956 0.907,274.937 0.907 L 272.450 0.907 270.952 3.953 C 270.128 5.629,269.448 7.000,269.442 6.999 C 269.435 6.999,268.756 5.628,267.932 3.953 L 266.435 0.907 263.971 0.907 C 262.009 0.907,261.509 0.913,261.518 0.936 M290.535 4.334 C 290.535 7.579,290.537 7.763,290.576 7.774 C 290.598 7.780,291.548 8.603,292.686 9.602 C 293.824 10.601,294.764 11.418,294.773 11.418 C 294.783 11.419,294.791 9.948,294.791 8.150 L 294.791 4.881 296.134 4.889 L 297.477 4.897 297.709 4.960 C 298.403 5.146,298.814 5.539,298.968 6.163 C 299.009 6.328,299.012 6.490,299.012 9.244 L 299.012 12.151 298.959 12.349 C 298.751 13.139,298.157 13.560,297.151 13.628 C 296.970 13.641,295.436 13.651,293.680 13.651 L 290.535 13.651 290.535 15.640 L 290.535 17.628 293.785 17.628 C 297.577 17.628,297.794 17.619,298.674 17.442 C 301.235 16.927,302.836 15.382,303.216 13.058 C 303.276 12.694,303.310 6.624,303.256 5.965 C 303.013 2.989,300.774 1.114,297.244 0.930 C 296.998 0.918,295.416 0.907,293.669 0.907 L 290.535 0.907 290.535 4.334 M305.512 9.267 L 305.512 17.628 311.337 17.628 L 317.163 17.628 317.163 15.616 L 317.163 13.605 313.488 13.605 L 309.814 13.605 309.814 12.372 L 309.814 11.140 313.186 11.140 L 316.558 11.140 316.558 9.302 L 316.558 7.465 313.186 7.465 L 309.814 7.465 309.814 6.186 L 309.814 4.907 313.488 4.907 L 317.163 4.907 317.163 2.907 L 317.163 0.907 311.337 0.907 L 305.512 0.907 305.512 9.267 M334.814 9.267 L 334.814 17.628 336.942 17.628 L 339.070 17.628 339.070 9.267 L 339.070 0.907 336.942 0.907 L 334.814 0.907 334.814 9.267 M341.674 9.267 L 341.674 17.628 347.198 17.628 L 352.721 17.628 352.721 15.523 L 352.721 13.419 349.326 13.419 L 345.930 13.419 345.930 7.163 L 345.930 0.907 343.802 0.907 L 341.674 0.907 341.674 9.267 M369.070 9.267 L 369.070 17.628 371.221 17.628 L 373.372 17.628 373.372 14.977 L 373.372 12.326 373.738 12.327 L 374.105 12.328 376.034 14.978 L 377.963 17.628 380.598 17.628 C 382.047 17.628,383.232 17.620,383.232 17.610 C 383.232 17.601,382.367 16.505,381.311 15.174 C 380.254 13.844,379.235 12.561,379.047 12.324 L 378.704 11.891 378.916 11.815 C 380.927 11.094,382.015 9.124,381.947 6.327 C 381.871 3.234,380.093 1.352,376.892 0.978 C 376.397 0.920,375.607 0.908,372.424 0.907 L 369.070 0.907 369.070 9.267 M87.395 4.380 C 87.395 7.647,87.398 7.832,87.436 7.843 C 87.458 7.850,88.408 8.672,89.547 9.672 C 90.685 10.671,91.624 11.488,91.634 11.488 C 91.643 11.488,91.651 9.918,91.651 7.998 L 91.651 4.508 93.017 4.517 C 94.332 4.526,94.391 4.528,94.565 4.576 C 95.987 4.971,96.023 6.916,94.616 7.389 L 94.430 7.452 93.436 7.460 L 92.442 7.468 92.442 9.000 L 92.442 10.532 93.483 10.541 C 94.659 10.550,94.662 10.550,95.070 10.750 C 96.268 11.337,96.266 13.127,95.067 13.706 C 94.587 13.937,94.724 13.930,90.785 13.930 L 87.395 13.930 87.395 15.791 L 87.395 17.651 90.901 17.651 C 94.484 17.650,94.947 17.641,95.592 17.558 C 98.238 17.219,99.773 15.793,100.173 13.306 C 100.464 11.494,99.636 9.754,98.063 8.875 C 97.831 8.745,97.832 8.747,97.947 8.686 C 98.883 8.188,99.526 7.007,99.522 5.791 C 99.514 3.345,97.984 1.554,95.488 1.071 C 94.834 0.944,94.944 0.947,91.029 0.937 L 87.395 0.927 87.395 4.380 M181.387 4.605 C 182.483 4.791,183.204 5.337,183.359 6.098 C 183.414 6.371,183.414 12.174,183.358 12.426 C 182.924 14.391,178.570 14.432,178.069 12.475 C 178.004 12.220,177.997 6.370,178.061 6.086 C 178.311 4.984,179.776 4.331,181.387 4.605 M391.352 4.603 C 392.415 4.786,393.110 5.288,393.318 6.023 C 393.384 6.258,393.384 12.254,393.318 12.488 C 392.775 14.411,388.490 14.392,388.036 12.464 C 387.983 12.238,387.982 6.267,388.035 6.057 C 388.309 4.975,389.775 4.332,391.352 4.603 M166.461 4.949 C 168.323 5.517,168.296 8.092,166.423 8.599 L 166.198 8.660 164.797 8.669 L 163.395 8.678 163.395 6.780 L 163.395 4.881 164.843 4.889 C 166.263 4.897,166.294 4.898,166.461 4.949 M376.423 4.947 C 378.081 5.414,378.313 7.706,376.779 8.453 C 376.357 8.659,376.206 8.674,374.634 8.674 L 373.372 8.674 373.372 6.778 L 373.372 4.882 374.808 4.889 C 376.199 4.896,376.250 4.898,376.423 4.947 M44.953 5.669 C 44.953 5.679,45.210 6.770,45.523 8.093 C 45.837 9.416,46.093 10.501,46.093 10.505 C 46.093 10.509,45.538 10.512,44.859 10.512 C 43.881 10.512,43.626 10.506,43.635 10.483 C 43.641 10.467,43.916 9.373,44.247 8.052 C 44.823 5.756,44.851 5.651,44.901 5.651 C 44.930 5.651,44.953 5.659,44.953 5.669 M108.742 8.052 C 109.054 9.373,109.314 10.467,109.320 10.483 C 109.328 10.506,109.073 10.512,108.093 10.512 C 107.113 10.512,106.858 10.506,106.865 10.483 C 106.871 10.467,107.147 9.373,107.478 8.052 C 108.029 5.862,108.085 5.651,108.128 5.651 C 108.171 5.651,108.222 5.849,108.742 8.052"></path></svg>') !important;
	display: inline !important;
	position: absolute !important;
	left: unset !important;
	bottom: 7px !important;
	top: unset !important;
	right: 15px !important;
	opacity: 0.3 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
	pointer-events: none !important;
	z-index: -1 !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i > div.sidebarRegion-VFTUkN > div.sidebarRegionScroller-3MXcoP.thin-1ybCId.scrollerBase-289Jih.fade-2kXiP2 > nav.sidebar-CFHs9e > div.side-8zPYf6 > div.info-1VyQPT {
	position: relative !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i > div.sidebarRegion-VFTUkN > div.sidebarRegionScroller-3MXcoP.thin-1ybCId.scrollerBase-289Jih.fade-2kXiP2 > nav.sidebar-CFHs9e > div.side-8zPYf6 > div.info-1VyQPT::after {
	content: "BasicBackground by" !important;
	font-size: 12px !important;
	color: var(--text-muted) !important;
	cursor: pointer !important;
	display: inline !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	cursor: text !important;
	visibility: visible !important;
	position: relative !important;
	top: unset !important;
	left: unset !important;
	bottom: unset !important;
	right: unset !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-3lHmkl > div.app-1q1i1E > div.app-2rEoOp > div.layers-3iHuyZ.layers-3q14ss > div.layer-3QrUeG.baseLayer-35bLyl + div.layer-3QrUeG > div.standardSidebarView-3F1I7i > div.sidebarRegion-VFTUkN > div.sidebarRegionScroller-3MXcoP.thin-1ybCId.scrollerBase-289Jih.fade-2kXiP2 > nav.sidebar-CFHs9e > div.side-8zPYf6 > div.info-1VyQPT::before {
	content: "DevilBro" !important;
	font-size: 12px !important;
	color: rgb(var(--accentcolor)) !important;
	display: inline !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	cursor: pointer !important;
	visibility: visible !important;
	position: absolute !important;
	top: unset !important;
	left: 113px !important;
	bottom: 9px !important;
	right: unset !important;
	transform: unset !important;
	animation: unset !important;
}
