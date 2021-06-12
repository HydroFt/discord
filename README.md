/* 
 * Yes, this codebase is near unreadable. Why?
 * I designed this mainly as a test to see how viable avoidance of straight out class selectors would be.
 * The codebase was never designed to be pretty, it was designed to require as little maintenance as possible.
 */

@import url('https://fonts.googleapis.com/css2?family=Karla:wght@400;500;600;700&display=swap');
@import url('https://mwittrien.github.io/BetterDiscordAddons/Themes/BlurpleRecolor/BlurpleRecolor.css');
@import url('https://discord-custom-covers.github.io/usrbg/dist/usrbg.css');

button {
	--accentcolor: var(--accent-alt);
}


/* Root Variables */

 racine {
	--transparencycolor: 0,0,0;
	--transparence alpha : 0,15 ;
	--transparence du message : 0,5 ;
	--usechatbubbles: calc(var(--messagetransparency) / (var(--messagetransparency) + 0,00000000000000000000001));
	--guildchanneltransparency : 0,15 ;
	--chatinputtransparency: 0.0;
	--memberlisttransparency: 0.0;
	
	--font : Whitney, Helvetica Neue, Helvetica, Arial, sans empattement ;
	--textshadow : transparent ;
	
	--couleur accent: 190,78,180;
	--accentcolor2: var(--accentcolor);
	--linkcolor: var(--accentcolor);
	
	--successcolor : 59,165,92 ;
	--warningcolor: 250,166,26;
	--dangercolor: 237,66,69;
	
	--textbrightest: 255,255,255;
	--textbrighter: 222,222,222;
	--textbright : 200 200 200 ;
	--textdark: 160,160,160;
	--texte plus sombre : 125 125 125 ;
	--textdarkest: 90,90,90;
	
	--background: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BasicBackground/_res/background.jpg);
	--backgroundposition : centre ;
	--backgroundsize : couverture ;
	--backgroundblur : non défini ;
	
	--popout: var(--background);
	--popoutposition: var(--backgroundposition);
	--popoutsize: var(--backgroundsize);
	--popoutblur: var(--backgroundblur);
	
	--backdrop: rgba(0,0,0,0.85);
	--backdropposition: var(--backgroundposition);
	--backdropsize: var(--backgroundsize);
	--backdropblur: var(--backgroundblur);
	
	--bdfdb-green: rgb(var(--successcolor));
	--bdfdb-jaune : rgb(var(--warningcolor));
	--bdfdb-red: rgb(var(--dangercolor));
}

.theme-dark,
.theme-light {
	/* Discord vars */
	--background-primary: var(--background-solid);
	--background-mobile-primary: var(--background-primary);
	--background-secondary: var(--background-solid);
	--background-mobile-secondary: var(--background-secondary);
	--background-secondary-alt: var(--background-solid);
	--background-tertiary: var(--background-solid);
	--background-floating: var(--background-solid);
	--background-secondary: var(--background-solid);
	--background-accent: var(--background-solid);
	--background-message-hover: rgba(var(--black), 0.4);
	--channeltextarea-background: transparent;
	--activity-card-background: rgba(var(--white), 0.05);
	--deprecated-store-bg: transparent;
	--background-modifier-hover: rgba(var(--black), 0.3);
	--background-modifier-active: rgba(var(--black), 0.3);
	--background-modifier-selected: rgba(var(--black), 0.6);
	--elevation-low: inset 0 -1px 0 0 rgba(var(--black), 0.3);
	--channels-default: rgba(var(--white), 0.3);
	--deprecated-quickswitcher-input-background: var(--background-solid);
	--header-primary: rgba(var(--white), 1);
	--header-secondary: rgba(var(--white), 0.6);
	--text-normal: rgba(var(--white), 0.6);
	--text-muted: #8a8e94;
	--interactive-muted: rgba(var(--white), 0.15);
	--interactive-normal: rgba(var(--white), 0.5);
	--interactive-hover: rgba(var(--white), 0.75);
	--interactive-active: rgba(var(--white), 1);
	--deprecated-card-bg: rgba(var(--white), 0.05);
	--text-link: rgba(var(--accent), 1);
	--focus-primary: rgba(var(--accent), 1);
}

 ::selection {
	background-color: rgba(var(--accent-alt), 0.5);
}


/* Scrollbars */

 ::-webkit-scrollbar {
	width: 14px !important;
}

 ::-webkit-scrollbar-thumb {
	border-radius: 8px !important;
	border: none !important;
	border: 3px solid transparent !important;
	background-color: rgba(var(--accent-alt), 1) !important;
}

 ::-webkit-scrollbar-track {
	visibility: visible !important;
	border-radius: 8px !important;
	border: 3px solid transparent !important;
	background-color: rgba(0, 0, 0, 0.3) !important;
	background-clip: padding-box !important;
}

.none-2Eo-qx::-webkit-scrollbar {
	display: none !important;
}


/* Titlebar */

div[class*="typeWindows-"] {
	--background-modifier-hover: rgba(var(--white), 0.05);
	--background-modifier-active: rgba(var(--white), 0.075);
	height: 26px;
}

div[class*="typeWindows-"]>div:first-child {
	display: none;
}

div[class*="typeWindows-"]>div[role="button"] {
	height: 30px;
	width: 36px;
}

div[class*="typeWindows-"]::after {
	content: 'Discord';
	font-weight: 5000;
	line-height: 31px;
	color: var(--text-muted);
	font-size: 14px;
	position: absolute;
	padding: 0 12px;
	top: 0;
	left: 0;
	width: 100%;
	height: 30px;
	background: rgba(var(--black), 0.85);
	z-index: -1;
}


/* Guilds */

ul[data-list-id='guildsnav'] {
	--background-secondary: var(--background-solid);
    	--background-primary: rgba(var(--white), 0.1);
	margin-bottom: 70px;
	background-color: rgba(var(--black), 0.6);
	border-right: 1px solid rgba(var(--black), 0.2);
	box-shadow: inset -10px 0px 20px -10px rgba(var(--black), 0.3);
}

ul[data-list-id='guildsnav'] ::-webkit-scrollbar {
	display: none;
}

ul[data-list-id='guildsnav']>div[dir] {
	padding-top: 18px;
}

ul[data-list-id='guildsnav'] [class^="pill-"],
ul[data-list-id='guildsnav'] [class^="pill-"]>div {
	height: 40px !important;
}

ul[data-list-id='guildsnav'] div[style*="height: 56"],
ul[id^="folder-items-"] {
	height: auto !important;
}

ul[data-list-id='guildsnav'] [class^="pill-"] span {
	width: 10px;
	margin-left: -5px;
	border-radius: 20px;
}

[data-list-id='guildsnav'] [class^="pill-"] span[style^="opacity: 1; height: 40"] {
	--header-primary: rgba(var(--accent), 1);
}

span[class^="expandedFolderBackground-"] {
	--background-secondary: rgba(var(--black), 0.25);
	border-radius: 14px;
	width: 40px;
	left: 16px;
}

.wrapper-25eVIn {
	zoom: .83334;
}

svg[class^="placeholderMask-"] {
	width: 40px;
	height: 40px;
}

div[data-list-item-id="guildsnav___home"] {
	background: var(--home-image) top center/110% no-repeat;
}

div[class^="unreadMentionsIndicatorBottom-"] {
	bottom: 70px;
}

#app-mount [data-list-item-id="guildsnav___home"]>div {
	color: transparent;
	background-color: transparent;
}

div[data-list-item-id="guildsnav___create-join-button"],
div[data-list-item-id="guildsnav___guild-discover-button"] {
	transition: 150ms ease;
	opacity: 0.5;
	background-color: var(--background-solid) !important;
	color: rgba(var(--white), 0.3) !important;
	border: 1px dashed rgba(var(--white), 0.3);
	border-radius: 50px;
}

div[data-list-item-id="guildsnav___create-join-button"]:hover,
div[data-list-item-id="guildsnav___guild-discover-button"]:hover {
	opacity: 1;
}


/* Sidebar */

.platform-win [class^="sidebar-"] {
	border-radius: 0;
}

div[class^="sidebar-"] nav,
#private-channels {
	background-color: transparent;
	--background-tertiary: rgba(var(--black), 0.35);
}

div[class^="sidebar-"]>nav>div[class^="searchBar"] {
	height: 54px;
}

div[id^="members-"] {
	--background-secondary: rgba(var(--black), 0.4);
	--background-modifier-hover: rgba(var(--white), 0.07);
	--background-modifier-active: var(--background-modifier-hover);
	--background-modifier-selected: rgba(var(--white), 0.07);
}

div[id^="members-"]>div {
	background-color: transparent;
}

div[id^="members-"] [class*="placeholder"] {
	--backgorund-primary: var(--text-normal);
}

div[class^='nowPlayingColumn'] {
	--background-secondary: transparent;
	--background-primary: rgba(var(--black), 0.5);
	--background-modifier-hover: rgba(var(--white), 0.075);
}

#channels div[class^="unread-"] {
	--interactive-active: rgba(var(--accent), 1);
}


/* Sidebar Header */

div[class*='clickable-'][aria-expanded]>header {
	height: 54px;
	--background-accent: rgba(var(--accent), 1);
	--background-modifier-hover: rgba(var(--black), 0.25);
}


/* Outer containers */

#app-mount {
	--background-tertiary: transparent;
	--background-secondary: transparent;
	background: var(--background-image) center/cover no-repeat;
}

#app-mount>div[class^="app-"] {
	--background-tertiary: transparent;
	--background-secondary: rgba(var(--black), 0.7);
	background-color: rgba(var(--black), 0.4);
}

nav+div [class^='sidebar-'],
nav+div[class^='base-'] {
	overflow: visible !important;
	position: relative;
	max-width: calc(100% - 72px);
}

nav+div[class^='base-'] > div[class^="notice"] {
	border-radius: 0;
}

div[class^='base-']>div {
	--background-secondary: rgba(var(--black), 0.7);
	--background-tertiary: rgba(var(--white), 0.05);
	--background-primary: rgba(var(--black), 0.8);
}

#app-mount>div:not([class^="app-"]),
.autocomplete-1vrmpx {
	--background-primary: var(--background-solid);
	--background-secondary: var(--background-solid-dark);
	--background-secondary-alt: var(--background-solid-darker);
	--background-tertiary: var(--background-solid-darker);
}


/* Header */

section[class*="themed-"] {
	height: 54px;
	box-shadow: var(--elevation-low);
	--background-secondary: rgba(var(--white), 0.1);
}

section>div>a[href="https:https://support.discord.com"] {
	display: none;
}

section[class*="themed-"]::before,
section[class*="themed-"] ::after {
	content: none;
}

section div[class^="toolbar"]>div[role] {
	margin: 0 4px;
	transition: 150ms ease;
	display: flex;
	align-items: center;
	justify-content: center;
	border-radius: 3px;
	width: 28px;
	height: 28px;
}

section div[class^="toolbar"]>div[role] svg {
	width: 22px;
}

section div[class^="toolbar"]>div[role][class*="selected-"] {
	background-color: rgba(var(--white), 0.1);
}


/* Panels */

div[class^='sidebar-']>section {
	--background-primary: rgba(var(--white), 0.07);
	--background-secondary: rgba(var(--white), 0.1);
	--background-secondary-alt: rgba(var(--black), 0.95);
	margin-bottom: 70px;
}

div[class^='sidebar-']>section>div:last-child {
	background-color: var(--background-secondary-alt);
	box-sizing: border-box;
	height: 70px;
	padding: 0 18px;
	width: calc(100% + 72px);
	position: absolute;
	left: -72px;
}


/* Content */

div[class^='chat'] {
	--background-floating: rgba(var(--black), 0.5);
}

div[class^="container-"][id^="chat-messages-"] {
	--background-modifier-hover: var(--background-solid-dark);
}

div[class^='chat'] main form {
	margin-top: 0;
}

div[class^='chat'] main form::before {
	content: none;
}

div[data-list-id="chat-messages"] {
	--background-primary: transparent;
	--background-secondary: rgba(var(--white), 0.05);
	--background-accent: rgba(var(--white), 0.1);
}

div[class^="channelTextArea-"] {
	--background-secondary: transparent;
	box-shadow: inset 0 0 0 2px rgba(var(--white), 0.1);
	transition: 250ms ease;
	margin-bottom: 24px;
	margin-top: 12px;
	border-radius: 5px;
}

div[id^="chat-messages-"]+div:not([id]):last-child {
	height: 8px;
}

div[id^="chat-messages-"][class*="cozy-"] {
	padding-left: calc(var(--avatar-size) * 2);
}

div[id^="chat-messages-"] {
	margin-left: 8px;
	margin-right: 8px;
	border-radius: 4px;
}

div[id^="chat-messages-"]>div[class^="buttonContainer-"] {
	transform: scale(.85);
	top: 1px;
}

div[id^="chat-messages-"] {
	--background-primary: rgba(var(--black), 0.5);
}

div[id^="chat-messages-"]>div>[class^="avatar-"] {
	margin-top: 6px;
	width: var(--avatar-size);
	height: var(--avatar-size);
}

div[id^="chat-messages-"][class*="cozy-"] div::before {
	--gutter: 13px;
}

.mention {
	transition: 150ms ease;
	color: rgba(var(--accent), 1) !important;
	background-color: rgba(var(--accent), 0.3);
	padding: 3px 5px;
	border-radius: 5px;
}

.mention:hover {
	background-color: rgba(var(--accent), 0.3) !important;
}

#app-mount .container-1D34oG {
	background: var(--background-primary);
}

div[class*="barBase-"] {
	padding-bottom: 0;
	background-color: rgba(var(--accent-alt), 0.9);
}


/* Codeblocks */

html pre {
	border-radius: 0;
	background: transparent;
	border-color: rgba(255, 255, 255, 0.1);
}

pre code.hljs {
	border: none;
	background-color: rgba(var(--white), 0.1);
	color: rgba(var(--white), 0.7);
	padding: 1em;
}

html code.inline,
html code.inline {
	background: rgba(var(--white), 0.1);
	color: rgba(var(--white), 0.7);
	padding: 0.3em 0.6em;
	border-radius: 3px;
}


/* Settings */

div[aria-label*="_SETTINGS"],
div[aria-label*="_DEBUG"] {
	--background-primary: transparent;
	--background-secondary: rgba(var(--black), 0.7);
}

div[class^="sidebarRegionScroller-"]>nav {
	--background-secondary: transparent;
}

div[class^="contentRegion-"] {
	--background-primary: rgba(var(--black), 0.8);
}

div[class^="contentRegion-"] div[style^="overflow: hidden scroll"] {
	background-color: transparent;
	--background-primary: rgba(var(--black), 0.1);
	--background-secondary: rgba(var(--black), 0.2);
	--background-secondary-alt: rgba(var(--black), 0.25);
	--background-tertiary: rgba(var(--white), 0.1);
}

div[aria-label*="_SETTINGS"] aside>div {
	--background-primary: transparent;
}

div[aria-label*="_SETTINGS"] aside>div::-webkit-scrollbar-track {
	visibility: hidden !important;
}

.bd-addon-list {
	--background-secondary: var(--background-solid);
	--background-secondary-alt: var(--background-solid-dark);
}


/* Tab Bar */

div[class*="topPill"],
nav>div[role="tablist"],
.bd-tab-bar {
	--background-accent: rgba(var(--accent));
	--background-modifier-hover: rgba(var(--white), 0.05);
	--background-modifier-active: rgba(var(--white), 0.075);
	--background-modifier-selected: rgba(var(--accent), 0.25);
}


/* Server Discovery */

div[class^="sidebar"]+[class^="pageWrapper"] {
	--background-secondary: rgba(var(--black), 0.8);
	background-color: var(--background-secondary);
}


/* Crash Page */

div[class*="errorPage"] {
	--background-secondary: rgba(var(--black), 0.7) !important;
}


/* Tooltips */

div[class^="tooltip-"] {
	--background-floating: rgba(var(--accent-alt), 1);
	--text-normal: #e0e0e0;
}


/* Buttons */

button[class*="button-"][class*="color"],
.bd-button {
	--vaccentcolor: var(--accent-alt);
}

.bd-button {
	--bd-blue: rgba(var(--accent-alt), 1);
}


/* Context Menu */

div[role="menuitem"] {
	--vaccentcolor: var(--accent-alt);
}

div[role="menuitem"]:active {
	--vaccentcolor: var(--accent);
}


/* Depreceated Components */


/* These use hardcoded colors, no need to bother with strange selectors */

#app-mount .footer-2gL1pp,
#app-mount .footer-3mqk7D {
	background-color: var(--background-secondary);
	box-shadow: none;
}

#app-mount .root-1gCeng,
#app-mount .addGamePopout-2RY8Ju,
#app-mount .keyboardShortcutsModal-3piNz7,
#app-mount .emojiAliasInput-1y-NBz .emojiInput-1aLNse,
.perksModal-fSYqOq .perk-2WeBWW,
#app-mount .uploadModal-2ifh8j,
#app-mount .contentWrapper-3WC1ID,
#app-mount .contentWarningPopout-n5JsIs {
	background-color: var(--background-primary);
}

#app-mount .codeRedemptionRedirect-1wVR4b,
#app-mount .userSettingsVoice-iwdUCU .previewOverlay-2O7_KC,
#app-mount .inset-3sAvek {
	background-color: var(--background-tertiary);
	border: none;
}

#app-mount .paymentPane-3bwJ6A,
#app-mount .tierBody-x9kBBp,
#app-mount .tierBody-16Chc9,
#app-mount .barBackground-2EEiLw,
#app-mount .body-3iLsc4,
#app-mount .footer-1fjuF6,
#app-mount .container-3ayLPN,
#app-mount .colorPickerCustom-2CWBn2,
#app-mount .tierMarkerBackground-3q29am,
.css-3vaxre-menu,
.css-dwar6a-menu,
#app-mount .autocomplete-1vrmpx,
.categoryHeader-O1zU94,
#app-mount .popoutList-T9CKZQ,
#app-mount .quickSelectPopout-X1hvgV,
.colorable-1bkp8v.primaryDark-3mSFDl,
.tile-2naSqK,
.videoWrapper-2v09vt,
#app-mount .spoilerText-3p6IlD.hidden-HHr2R9 {
	background-color: var(--background-solid);
}

#app-mount .expandedInfo-3kfShd,
#app-mount .tierHeaderLocked-1a2opw,
#app-mount .tierHeaderLocked-1s2JJz,
#app-mount .headerNormal-T_seeN,
#app-mount .focused-2bY0OD,
.colorable-1bkp8v.primaryDark-3mSFDl:hover {
	background-color: var(--background-solid-dark);
}

#app-mount .payment-xT17Mq {
	background-color: transparent;
	border-bottom-color: rgba(var(--white), 0.025);
}

#app-mount .bottomDivider-1K9Gao,
#app-mount .focused-2bY0OD {
	border-bottom-color: var(--background-solid-dark);
}

#app-mount div[data-list-id="billing-history"],
#app-mount .media-engine-video,
.react-datepicker,
.react-datepicker__header,
.react-datepicker__day--outside-month,
.react-datepicker__day--disabled {
	background-color: transparent !important;
}

.react-datepicker__day--disabled {
	opacity: .6;
}

#app-mount .react-datepicker__day {
	border-top-color: var(--background-secondary);
	border-left-color: var(--background-secondary);
}

#app-mount .background-3xPPFc,
#app-mount .tierInProgress-3mBoXq {
	color: var(--background-solid);
}

.option-96V44q:after {
	content: none;
}

#app-mount .option-96V44q.selected-rZcOL-,
#app-mount .selected-1Tbx07,
#app-mount .quickSelectPopoutOption-opKBx9:hover,
#app-mount .outer-1AjyKL.active-1xchHY,
#app-mount .outer-1AjyKL.interactive-3B9GmY:hover {
	background-color: var(--background-modifier-hover);
}

.css-3vaxre-menu,
.tierMarker-5HkGJ_[style] {
	border-color: rgba(var(--white), 0.025) !important;
}

#app-mount .searchAnswer-3Dz2-q,
#app-mount .searchFilter-2ESiM3,
#app-mount .option-1B5ZV8,
#app-mount .pill-2pQByF {
	background-color: rgba(var(--accent-alt), 1);
	color: #fff;
}

#app-mount .keybindShortcut-1BD6Z1 span {
	background: var(--background-solid-dark);
	box-shadow: inset 0 -4px 0 var(--background-solid-darker);
}

#app-mount .perksModal-fSYqOq {
	background: rgba(var(--black), 0.7);
}

#app-mount .card-FDVird:before {
	background: var(--background-modifier-hover);
	border: none;
}


/* Login Page */

div[class^="splashBackground"] canvas,
div[class^="splashBackground"] img {
	display: none;
}

/* USRBG */

/*
 * USRBG User-Popout Implimentation
 * 
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
*/

.userPopout-3XzG_A {
	overflow: hidden;
	transform: translateZ(0) !important;
	--USRBG-banner-height: 60px;
}

.userPopout-3XzG_A[style*="-user-"] {
	--USRBG-banner-height: 120px;
	--USRBG-avatar-offset: 76px;
}

.userPopout-3XzG_A[style*="-user-"] .profileBanner-33-uE1 {
	background-size: cover;
	background-repeat: no-repeat;
	background-position: var(--user-popout-position, center) center;
	background-image: var(--user-background);
}

.userPopout-3XzG_A[style*="-user-"] .profileBanner-33-uE1 {
	height: var(--USRBG-banner-height, 120px);
}

.userPopout-3XzG_A[style*="-user-"] .avatarWrapperNormal-2tu8Ts {
  	top: var(--USRBG-avatar-offset, 76px);
}

.userPopout-3XzG_A:not([style*="-user-"]) .avatar-22FtUu,
.userPopout-3XzG_A:not([style*="-user-"]) .avatarHint-1E3LMl{
	z-index: 1;
}

.userPopout-3XzG_A:not([style*="-user-"]) .avatar-22FtUu::after {
	content: '';
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	z-index: -1;
	height: var(--USRBG-banner-height, 60px);
	pointer-events: none;
	background-size: cover;
	background-repeat: no-repeat;
	background-position: var(--user-popout-position, center) center;
	background-image: var(--user-background);
}
