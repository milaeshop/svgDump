let totalMessages = 0, channelName;
let hideCommands = "no";
let ignoredUsers = [];
let msgQueue = [];
let msgAlign, currency = "";
let fieldData, largeEmotes, badgesCustom, badgesDisplay, userType, pronounsOn;
let pronounsCache = {};
let counter = 0, counterEmotes = 0;
let emotesStorage = [], providerID;
let emoteOnly = false;
let pronounsbadge, pronounsObj = {
pronouns: {}};
let clinetId = "3sqjke05n4hysdkxrv3ufoqvwuwdxc";
let clinetSecret = "g05nmdek9fb61gt2qjksxqxc3wc5zm";
let dataD;
let userImageLoaded = {};
let bitspecial = 0, subspecial = 0, tipspecial = 0, minRaid = 0;
let beingAnimated = false;
let sum = 0;
let timechange = 4;
let emoteIsGif = false;
let testSession;
let countNames = 0;
const leaders = {
  topAlltimeSubGiftUsername: {name: "", amount: ""},
  topAlltimeCheerUsername : {name: "", amount: ""},
  topSessionCheerUsername : {name: "", amount: ""},
  topMonthlyCheerUsername : {name: "", amount: ""},
};

let iconsObj = fillIconsObj();
let socialsIcons = fillSocialsObj();

let redeemIc = getRedeemIc();
let newtopcheeric = getnewtopcheeric();
let newtopgiftic = getnewtopgiftic();

  const PRONOUNS_API_BASE = 'https://pronouns.alejo.io/api'
  const PRONOUNS_API = {
  user: username => `${PRONOUNS_API_BASE}/users/${username}`,
  pronouns: `${PRONOUNS_API_BASE}/pronouns`,
}

  async function getPronouns() {
  const res = await get(PRONOUNS_API.pronouns)
  if (res) {
    res.forEach(pronoun => {
      pronounsObj.pronouns[pronoun.name] = pronoun.display
    })
  }
}
let dotf = `<svg class="dotf" width="6" height="6" viewBox="0 0 6 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path cx="3.383" cy="2.722" r="2.5" fill="var(--col2)" d="M5.883 2.722A2.5 2.5 0 0 1 3.383 5.222A2.5 2.5 0 0 1 0.883 2.722A2.5 2.5 0 0 1 5.883 2.722z"/></svg>`
let header = `<svg class="header" width="76" height="9" viewBox="0 0 76 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M71.034 0.03c2.25 0 4.073 1.876 4.073 4.19 0 2.316 -1.823 4.192 -4.073 4.192 -2.249 0 -4.072 -1.876 -4.072 -4.191S68.785 0.029 71.034 0.029M4.302 0.03h48.492c2.25 0 4.072 1.876 4.072 4.19 0 2.316 -1.823 4.192 -4.072 4.192H4.302C2.053 8.412 0.23 6.536 0.23 4.221S2.053 0.029 4.302 0.029" fill="var(--alertbg)"/></svg>`
let subdecor = `<svg class="subdecor2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 38.85 32.02" width="38.85" height="32.02">
    <path class="qmark" d="M16.09 18.09a2.756 2.756 0 0 1 -1.03 -3.54l3.91 -8.12a2.76 2.76 0 0 1 3.94 -1.15l1.64 1.02c1.39 0.87 1.73 2.75 0.72 4.04l-5.55 7.1a2.75 2.75 0 0 1 -3.63 0.64Zm-1.82 2.93a2.367 2.367 0 1 0 -2.5 4.02 2.367 2.367 0 0 0 2.5 -4.02" style="fill:var(--col2);transform-origin: 18px 15px;"/>
    <path class="ap1" cx="1.98" cy="1.98" r="1.98" style="fill:var(--col2)" d="M3.96 1.98A1.98 1.98 0 0 1 1.98 3.96A1.98 1.98 0 0 1 0 1.98A1.98 1.98 0 0 1 3.96 1.98z"/>
    <path class="ap1" cx="37.92" cy="5.39" r="1.98" style="fill:var(--col2)" d="M3.96 1.98A1.98 1.98 0 0 1 1.98 3.96A1.98 1.98 0 0 1 0 1.98A1.98 1.98 0 0 1 3.96 1.98z"/>
    <path class="ap2" d="M37.77 27.38h-1.72v-1.72c0 -0.54 -0.43 -0.97 -0.97 -0.97s-0.97 0.43 -0.97 0.97v1.72h-1.72c-0.54 0 -0.97 0.43 -0.97 0.97s0.43 0.97 0.97 0.97h1.72v1.72c0 0.54 0.43 0.97 0.97 0.97s0.97 -0.43 0.97 -0.97v-1.72h1.72c0.54 0 0.97 -0.43 0.97 -0.97s-0.43 -0.97 -0.97 -0.97" style="fill:var(--col2)"/>
    <path class="ap3" cx="37.92" cy="5.39" r="1" style="fill:var(--col2)" d="M38.85 5.39A0.93 0.93 0 0 1 37.92 6.32A0.93 0.93 0 0 1 36.99 5.39A0.93 0.93 0 0 1 38.85 5.39z"/>
  </svg>`
let subdots = `<svg class="subdots" width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6.94 0.282h0.012c0.889 0 1.609 0.72 1.609 1.608v8.967c0 0.888 -0.72 1.608 -1.609 1.608H6.94c-0.888 0 -1.608 -0.72 -1.608 -1.608V1.89c0 -0.888 0.72 -1.608 1.608 -1.608" fill="var(--col1)"/><path d="M13.047 6.36v0.013c0 0.888 -0.72 1.608 -1.609 1.608H2.467c-0.889 0 -1.609 -0.72 -1.609 -1.608V6.36c0 -0.888 0.72 -1.608 1.609 -1.608h8.971c0.888 0 1.609 0.72 1.609 1.608M28.94 30.278a1.909 1.909 0 1 1 0.033 -3.818 1.909 1.909 0 0 1 -0.032 3.817" fill="var(--col1)"/></svg>`
let warning = `<svg class="warning" width="12" height="37" viewBox="0 0 12 37" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path fill-rule="evenodd" clip-rule="evenodd" d="M5.772.314q-2.896.03-4.113 2.4Q.485 5.033.509 8.442c.014 1.705.17 4.444.47 6.546q.45 3.105 1.236 5.603a5.3 5.3 0 0 0 1.337 2.192q.943.892 2.392.877 1.447-.016 2.335-.927a5.35 5.35 0 0 0 1.304-2.22q.747-2.565 1.148-5.778c.268-2.175.395-4.984.381-6.756q-.024-3.209-1.32-5.45Q8.542.284 5.773.313m.04 36.42a4.166 4.166 0 1 0-.001-8.33 4.166 4.166 0 0 0 0 8.33" fill="#D9D9D9"/>
  <path fill-rule="evenodd" clip-rule="evenodd" d="M5.772.314q-2.896.03-4.113 2.4Q.485 5.033.509 8.442c.014 1.705.17 4.444.47 6.546q.45 3.105 1.236 5.603a5.3 5.3 0 0 0 1.337 2.192q.943.892 2.392.877 1.447-.016 2.335-.927a5.35 5.35 0 0 0 1.304-2.22q.747-2.565 1.148-5.778c.268-2.175.395-4.984.381-6.756q-.024-3.209-1.32-5.45Q8.542.284 5.773.313m.04 36.42a4.166 4.166 0 1 0-.001-8.33 4.166 4.166 0 0 0 0 8.33" fill="url(#awarning)"/>
  <defs>
    <linearGradient id="awarning" x1="5.368" y1="2.724" x2="5.368" y2="36.959" gradientUnits="userSpaceOnUse">
      <stop stop-color="var(--col1)"/>
      <stop offset="1" stop-color="var(--col2)"/>
    </linearGradient>
  </defs>
</svg>`;
let arrow2 = `<svg class="arrow" width="34" height="19" viewBox="0 0 34 19" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M26.146 1.745a1.767 1.767 0 0 0 -2.499 0h0c-0.69 0.69 -0.69 1.809 0 2.499l0.354 -0.354 -0.354 0.354 3.796 3.796H2.885a1.767 1.767 0 0 0 0 3.534h24.558l-3.796 3.796a1.767 1.767 0 1 0 2.499 2.5l6.813 -6.814c0.69 -0.69 0.69 -1.808 0 -2.498z" fill="var(--arrowscol)" stroke="var(--arrowscol)" stroke-linecap="round" stroke-linejoin="round" stroke-width="1"/></svg>`;
let dotsraid = `<svg class="dots11" width="22" height="23" viewBox="0 0 22 23" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M16.649.244h-.011c-.743 0-1.346.602-1.346 1.345v7.5c0 .744.603 1.346 1.346 1.346h.01c.744 0 1.346-.602 1.346-1.345V1.589c0-.743-.602-1.345-1.345-1.345" fill="var(--col1)"/>
  <path d="M11.54 5.329v.01c0 .743.603 1.345 1.346 1.345h7.504c.743 0 1.345-.602 1.345-1.345v-.01c0-.743-.602-1.345-1.345-1.345h-7.504c-.743 0-1.345.602-1.345 1.345M1.726 22.236a1.46 1.46 0 1 0-.025-2.92 1.46 1.46 0 0 0 .025 2.92" fill="var(--col1)"/>
</svg>
<svg class="dots2" width="22" height="23" viewBox="0 0 22 23" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M16.649.244h-.011c-.743 0-1.346.602-1.346 1.345v7.5c0 .744.603 1.346 1.346 1.346h.01c.744 0 1.346-.602 1.346-1.345V1.589c0-.743-.602-1.345-1.345-1.345" fill="var(--col2)"/>
  <path d="M11.54 5.329v.01c0 .743.603 1.345 1.346 1.345h7.504c.743 0 1.345-.602 1.345-1.345v-.01c0-.743-.602-1.345-1.345-1.345h-7.504c-.743 0-1.345.602-1.345 1.345M1.726 22.236a1.46 1.46 0 1 0-.025-2.92 1.46 1.46 0 0 0 .025 2.92" fill="var(--col2)"/>
</svg>`;
let dots22 = `<svg class="dots2" width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M23.985.085h-.013c-.888 0-1.608.72-1.608 1.607v8.968c0 .888.72 1.608 1.608 1.608h.013c.889 0 1.609-.72 1.609-1.608V1.692c0-.888-.72-1.607-1.609-1.607" fill="var(--col2)"/>
  <path d="M17.878 6.163v.013c0 .888.72 1.608 1.608 1.608h8.972c.888 0 1.608-.72 1.608-1.608v-.013c0-.888-.72-1.608-1.608-1.608h-8.971c-.889 0-1.609.72-1.609 1.608M1.984 30.08a1.909 1.909 0 1 0-.032-3.818 1.909 1.909 0 0 0 .032 3.818" fill="var(--col2)"/>
</svg>`;
let dots11 = `<svg class="dots11" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 30.01 30" width="30.01" height="30"><path d="M28.4 4.47h-2.86V1.61c0 -0.89 -0.72 -1.61 -1.61 -1.61h-0.01c-0.89 0 -1.61 0.72 -1.61 1.61v2.86h-2.88c-0.89 0 -1.61 0.72 -1.61 1.61 0 0.9 0.72 1.62 1.61 1.62h2.88v2.88c0 0.89 0.72 1.61 1.61 1.61h0.01c0.89 0 1.61 -0.72 1.61 -1.61V7.7h2.86c0.89 0 1.61 -0.72 1.61 -1.61 0 -0.9 -0.72 -1.62 -1.61 -1.62" fill="var(--col1)"/><path d="M1.93 29.99c1.05 0 1.9 -0.87 1.89 -1.93s-0.87 -1.9 -1.93 -1.89A1.93 1.93 0 0 0 0 28.1c0 1.05 0.87 1.9 1.93 1.89" fill="var(--col1)"/></svg>`;

function addFollowerBlock(name, text, amount = "") {
  return `<div class="alertcont">  
           <div class="alerttextfol">
           <div class="switchbox"></div> 
           ${dotf}
          <div class="amal">${name} ${text}</div></div>
         </div>`
      }
      function addCheerBlock(name, text, amount = "") {
        return `<div class="alertcont">  
        <div class="alerttext">
        <div class="confettibox"></div>
        <div class="decorcont">
     <div class="weeew"></div>
     </div>
     ${icons.cheeric}
     ${header}
        <div class="nameal">${name}</div>
<svg class="arrow" width="34" height="19" viewBox="0 0 34 19" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M26.146 1.745a1.767 1.767 0 0 0 -2.499 0h0c-0.69 0.69 -0.69 1.809 0 2.499l0.354 -0.354 -0.354 0.354 3.796 3.796H2.885a1.767 1.767 0 0 0 0 3.534h24.558l-3.796 3.796a1.767 1.767 0 1 0 2.499 2.5l6.813 -6.814c0.69 -0.69 0.69 -1.808 0 -2.498z" fill="var(--arrowscol)" stroke="var(--arrowscol)" stroke-linecap="round" stroke-linejoin="round" stroke-width="1"/></svg>
<div class="amal"><span>${text}</span>
        <div class="amountal"><span>${amount}</span></div></div>
        </div>
      </div>`
      }
      function addTipBlock(name, text, amount = "") {
        return `<div class="alertcont">  
        <div class="alerttext">
        <div class="decorcont">
     <div class="weeew"></div>
     </div>
      <div class="curr1 yuik yuik2 leftchr" data-curr="${currency}"></div>
       <div class="curr2 yuik yuik2 rightchr" data-curr="${currency}"></div>
       ${header} 
        <div class="nameal">${name}</div>
${arrow2}
<div class="amal"><span>${text}</span>
        <div class="amountal"><span>${amount}</span></div></div>
 
        </div>
      </div>`
      }
  function addSubBlock(name, text, amount) {
  return `<div class="alertcont">  
           <div class="alerttext">
           <div class="decorcont">
   <div class="weeew"></div>
   </div>
  ${header}
<div class="nameal">${name}</div>
${arrow2}
<div class="amal"><span>${text}</span>
           <div class="amountal"><span>${amount}</span></div>
            </div>
           
           </div>
         </div>`
      }
  function addNewSubBlock(name, text, amount = "") {
   return `<div class="alertcont">  
           <div class="alerttext">
          ${subdots}
           <div class="decorcont">
   <div class="weeew"></div>
   </div>
     ${header}
<div class="nameal">${name}</div>
${arrow2}
<div class="amal">${text}
           <div class="amountal">
     ${subdecor}     
  <span>${amount}</span></div>
            </div>
           </div>
         </div>`
      }
     function addRaidBlock(name, text, amount = "") {
  return `<div class="alertcont">  
  <div class="alerttext popwin">
  ${header}
  </div>
  <div class="alerttext popwin">
  ${header}
  </div>
  <div class="alerttext wrng">
<div>
  ${warning}
</div>
<div>
  <div class="nameal">${name}</div><div class="amal">${text}</div></div>
${header}
${dotsraid}
<div class="decorcont">
   <div class="weeew"></div>
   </div>
</div>
  </div>`
      }
     function addGiftBlock(name, text, amount = "") {
      return `<div class="alertcont">  
      <div class="alerttext">
      <div class="decorcont">
   <div class="weeew"></div>
   </div>
${header}
      <div class="nameal">${name}</div>
${arrow2}
<div class="amal">${text}
      <div class="amountal"><span>${amount}</span></div>
       </div>
      </div>
    </div>`
      }

  function addMessage(username, badges, message, uid, msgId, userType, emoteOnly, replyBody, classToAdd, leaderBody) {  
    let pfpElement = "";
    msgQueue.unshift(username);
    if (!fieldData.hidepfp) {
    if (fieldData.pfptype == "pfpTwitch") {      
      if (userType == "default" && fieldData["pfp-subonly"]) {
    pfpElement = icons[`${userType}ic`]
   } else {
    pfpElement = `<div class="pfp-img id${uid}"></div>`
  }
   } else if (fieldData.pfptype == "upload") {
     pfpElement = fieldData[`${userType}pfp`] ? `<div class="pfp-img ${userType}upload uploadpfp">
   </div>` : icons[`${userType}ic`];
   } else if (fieldData.pfptype == "inits") {
pfpElement = `<div class="inits">${username[0]}</div>`
   } else {
    pfpElement = iconsObj[`${fieldData.pfptype}`][`${userType}`]
   }

    }
    totalMessages += 1;
    let actionClass = "";

if (badges != "" && badgesDisplay) {
    badges = `<div class="badgesbox"><div class="badgesdecorcont"><span></span><span></span><span class="bdg1"></span></div>
${badges}</div>`;
   } else badges = ""
// pfpoff   namebgon
if (fieldData.typewritenames) {
username = username.split("").map(el => el = `<span class="eventletter">${el}</span>`).join("") + `<span class="pointer eventletter">_</span>`
}
    let element = $.parseHTML(`<div data-sender="${uid}" data-msgid="${msgId}" class="message-row ${msgId} ${userType}style ${classToAdd}">
      <div class="anim msganim  {msgAlign} {anim} emoteonly${emoteOnly}">
        <div class="msgcont">
      <div class="namebox">
      <div>
     <svg class="dot defaulto artisto" width="6" height="6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 6 6">
  <circle cx="3" cy="3" r="3" style="fill:var(--col2)"/>
</svg>
     <span class="name">
     <span>
    ${username}</span>
    </span> 
    <span class="pronouns"></span> 
     </div>
      ${badges}
    </div> 
     <div class="messagebox">
     <div class="pfp pfp1">
     ${pfpElement}

${dots11}
</div>

${dots22}

     <div class="decorcont">
      </div>
       <div class="message">
     <span class="msg"><div>${message}</div></span>
     </div> 
     </div>
     </div>
    </div></div>`);
  
    if (msgAlign === "end") {
            $(element).appendTo('.main-container');
        }
     else {
            $(element).prependTo('.main-container');
        } 

if (!fieldData.msgbgoff && !(fieldData.pfptype == "none" || fieldData.hidepfp)) {
$(element).find(".pfp").detach().prependTo($(element).find(".anim"))
}
     $(element).hide();

     if (replyBody && fieldData.repliesOn) {
      $(element).addClass("namewrap").find(".name").after(replyBody);
      $(element).find(".badgesbox").remove()
      leaderBody = "";
    }

    if (leaderBody && fieldData.leaderTagsOn) {
if (!fieldData.msgbgoff) {
  $(element).addClass("namewrap").find(".name").after(leaderBody);
} else {
  $(element).find(".message").append(leaderBody)
}
 }


 if (fieldData.msgconnect) {

  if ($(element).prev().attr("data-sender") == uid) {
    $(element).addClass("nextmsg")
     $(element).prev().addClass("prevmsg").find(".dots2").remove()
   } 
  }

  if (emoteOnly) {
let emotesDisplay =  $(element).find(".emote").toArray();

if (emotesDisplay.length == 1 && fieldData.stickerEmote && !emoteIsGif) {
  
$(element).addClass("stickerEmote")
$(element).find(".emote").removeClass("large");
}
  }

    if (badgesDisplay === false) {
  $('.badgesbox').css("display", "none")
  }

  if (badges != "" && badgesDisplay) {
    $(".vip").html(`<svg class="svgbadge" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" version="1.1" id="svg902" viewBox="0 0 96 96">
    <defs id="defs906"/>
    <g id="g908">
      <path fill="var(--badgescol)" d="M 19.403191,10.959868 0.36376509,36.881015 47.159463,87.576356 95.560901,35.504671 76.292081,11.189259 Z" id="path916"/>
    </g>
  </svg>`); 
    $(".moderator").html(`<svg class="svgbadge" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" version="1.1" id="svg966" viewBox="0 0 96 96">
    <defs id="defs970"/>
    <g id="g972">
      <path fill="var(--badgescol)" stroke="var(--badgescol)" d="m 5.514926,89.698649 6.163741,6.001538 19.302241,-12.65189 13.1385,12.489686 8.110185,-7.785778 L 39.253297,76.073538 90.671872,29.196667 90.509668,0.97322224 56.771297,1.7842408 23.843945,62.448427 10.705445,51.742982 4.8661112,59.690964 16.706982,70.396408 Z" id="path976"/>
    </g>
  </svg>`)
    $(".broadcaster").html(`
  <svg class="svgbadge" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" viewBox="0 0 30.074135 21.467426" version="1.1" id="svg5" xml:space="preserve"><defs id="defs2"/><g id="layer1" transform="translate(-72.032296,-84.451693)"><path id="rect237" style="fill:var(--badgescol);stroke-width:0" d="m 76.467684,84.451693 c -2.457256,0 -4.435388,1.978132 -4.435388,4.435388 v 12.596649 c 0,2.45725 1.978132,4.43539 4.435388,4.43539 h 12.774414 c 2.457256,0 4.435388,-1.97814 4.435388,-4.43539 v -1.44074 l 8.403624,3.88762 0.0253,-8.658906 -0.3328,-8.654252 -8.096144,4.028178 v -1.758549 c 0,-2.457256 -1.978132,-4.435388 -4.435388,-4.435388 z"/></g></svg>
  `);
       $(".premium").html(`<svg class="svgbadge" width="258.166" height="258.166" viewBox="0 0 68.306 68.306" xml:space="preserve" xmlns="http://www.w3.org/2000/svg">
    <path style="fill:var(--badgescol);stroke-width:3.293;stroke-linecap:round;stroke-linejoin:round;-inkscape-stroke:none;paint-order:stroke fill markers" d="M100.243 106.668c-.419 0-.838.158-1.158.476L82.462 123.6l-12.86-11.883c-1.078-.997-2.823-.192-2.764 1.275l1.243 31.403a1.646 1.646 0 0 0 1.646 1.581h60.323c.877 0 1.6-.687 1.644-1.564l1.596-32.113c.074-1.505-1.743-2.31-2.809-1.246l-12.502 12.502-16.578-16.412a1.642 1.642 0 0 0-1.158-.476z" transform="translate(-65.823 -93.145)"/>
  </svg>`);
      $(".artist-badge").html(`<svg width="260.306" height="261.125" viewBox="0 0 260.306 261.125" xmlns="http://www.w3.org/2000/svg">
    <path style="fill:var(--badgescol);stroke:none;stroke-width:2.236;stroke-linecap:square;paint-order:markers stroke fill" d="M249.344 55.868s-49.869 46.12-66.367 73.49c0 0-44.62-8.248-65.242 35.621 0 0-4.124 9.75-3.374 20.998 0 0 4.43 12.464-21.816 36.086 0 0 60.06 4.784 85.183-8.34 25.122-13.123 26.996-44.244 26.621-47.619-.374-3.374-.374-16.498-.374-16.498l73.115-65.991s26.997 32.246 18.748 64.491c-8.249 32.246-17.998 36.746-36.37 57.368-18.373 20.623-17.248 10.499-18.748 31.871-1.5 21.373-17.998 50.994-54.368 58.868-36.37 7.874-82.115-9.374-91.864-16.123-9.749-6.75-56.618-37.87-57.368-96.738S55.868 93.363 70.491 79.115C85.114 64.867 116.235 36.37 163.48 37.12c47.244.75 68.991 2.25 85.864 18.748z" transform="translate(-37.1 -37.106)"/>
  </svg>`);
       $(".partner").html(`<svg width="19.6" height="19.598" viewBox="0 0 5.186 5.185" xml:space="preserve" xmlns="http://www.w3.org/2000/svg">
    <path style="opacity:1;fill:var(--badgescol);fill-opacity:1;stroke:none;stroke-width:.216527;stroke-linecap:round;stroke-linejoin:round;stroke-opacity:1;paint-order:stroke markers fill" d="M2.61 0 .772.747 0 2.575l.747 1.839 1.829.771 1.838-.747.772-1.828L4.439.77Zm.904 1.37.612.607L2.28 3.84l-.011-.01-.008.006-.567-.576-.026-.026-.625-.635.607-.613.624.635Z"/>
  </svg>
  `);
       }

   if (fieldData.userTyping) {
    msgQueue = [...new Set(msgQueue)];
    if (msgQueue.length <= 1) {$(".typingText").text(`${msgQueue[0]} is typing...`);
    } else if (msgQueue.length == 2) {
      $(".typingText").text(`${msgQueue[0]} and ${msgQueue[1]} are typing...`);
   } else if (msgQueue.length > 2) {
    $(".typingText").text("Multiple users are typing...");
   }
   
    $(".userTyping").fadeIn(200)
    $(".topic").fadeOut(200)
setTimeout(()=>{
msgQueue.shift();
  setTimeout(()=>{
    if (msgQueue == 0) {
      $(".topic").fadeIn(200)
      $(".userTyping").fadeOut(200)
    }
  }, 300)

 LimitMsg(element)
}, 1000)
} else {
LimitMsg(element);
element = null;
} 
  }

 let topsbIc = `<svg class="icon0" width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path opacity=".5" d="M14.68 3.344 2.456 5.5c-.52.091-.87.567-.782 1.063l.158.896c.088.496.58.823 1.098.732l3.291-.58c-1.039.183-1.739 1.135-1.564 2.126l.791 4.488c.175.991 1.159 1.646 2.198 1.463l7.993-1.409c.518-.091.869-.568.781-1.063l-1.266-7.18c.519-.09.87-.567.782-1.062l-.158-.897c-.088-.495-.58-.823-1.098-.731z"/>
  <path d="m14.175 3.046-1.795.317c.353-.953.213-1.857-.434-2.296-.883-.578-2.29-.038-3.21 1.226-.392.532-.63 1.111-.706 1.644-.254-.477-.676-.939-1.223-1.304C5.51 1.76 4 1.735 3.365 2.584c-.455.63-.275 1.525.383 2.302l-1.797.317C1.174 5.34.647 6.056.778 6.798l.158.897c.104.585.585 1.008 1.163 1.098l1.202 6.814c.13.742.87 1.235 1.647 1.097l10.343-1.823c.778-.137 1.304-.853 1.173-1.595l-.95-5.385a.467.467 0 0 0-.55-.366.467.467 0 0 0-.39.532l.949 5.385a.467.467 0 0 1-.391.532l-3.292.58-1.266-7.18 4.231-.745c.778-.138 1.304-.853 1.173-1.595l-.158-.897c-.13-.742-.87-1.235-1.648-1.098zm-4.662-.238c.627-.859 1.511-1.23 1.88-.99.318.217.303.968-.165 1.747l-2.238.394c.07-.366.249-.777.524-1.153zM4.141 3.1c.27-.36 1.226-.313 2.11.282.386.258.696.584.886.904l-2.238.395c-.71-.573-.98-1.273-.758-1.581M1.718 6.63a.467.467 0 0 1 .391-.532l4.231-.746.317 1.795-4.231.746a.467.467 0 0 1-.55-.366zm2.522 8.81L3.053 8.708l3.762-.663 1.266 7.18-3.291.58a.467.467 0 0 1-.55-.366zm4.78-.38L7.28 5.188l1.881-.331 1.74 9.872zm6.02-9.852a.467.467 0 0 1-.392.532l-4.23.746-.317-1.795 4.23-.746a.467.467 0 0 1 .55.366z"/>
</svg>`
let topchrIc = `<svg class="icon0 uio" width="32" height="29" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M4.423 4.745h-1.07v-1.07a.6.6 0 0 0-.602-.601h-.003a.6.6 0 0 0-.602.602v1.069H1.069a.6.6 0 0 0-.602.602c0 .336.269.606.602.606h1.077v1.076c0 .333.269.602.602.602h.003a.6.6 0 0 0 .602-.602V5.953h1.07c.332 0 .602-.27.602-.602a.6.6 0 0 0-.602-.606m26.891 21.087h-1.07v-1.07a.6.6 0 0 0-.602-.602h-.003a.6.6 0 0 0-.602.602v1.07H27.96a.6.6 0 0 0-.602.601c0 .337.269.606.602.606h1.077v1.077c0 .333.269.602.602.602h.003c.333 0 .602-.27.602-.602v-1.077h1.07a.6.6 0 0 0 .602-.602.6.6 0 0 0-.602-.605"/>
  <path d="m27.65 1.66-3.563 4.573a.63.63 0 0 0 .045.821l2.448 2.561a.64.64 0 0 0 .753.121l3.096-1.665c.271-.15.4-.474.294-.768l-1.981-5.47a.628.628 0 0 0-1.085-.172z" opacity=".6"/>
  <path d="M27.288 10.135a.98.98 0 0 1-.972-.271l-2.448-2.561a.994.994 0 0 1-.068-1.288l3.57-4.573.03-.037a.98.98 0 0 1 .905-.34c.361.06.648.302.776.64l1.981 5.47a.99.99 0 0 1-.46 1.205l-3.096 1.665c-.067.037-.135.06-.21.083zm.625-8.226-3.54 4.55a.263.263 0 0 0 .015.347l2.448 2.56c.083.084.21.106.316.054l3.096-1.665a.25.25 0 0 0 .12-.324l-1.98-5.47a.25.25 0 0 0-.211-.172.27.27 0 0 0-.256.098c0 .007-.015.015-.023.03z" stroke-width=".5" stroke="url(#aicon)"/>
  <path opacity=".5" d="M21.744 16.97a2590 2590 0 0 0-6.492-3.297.47.47 0 0 0-.567.102L9.8 18.883c-.353.372-.966 0-.808-.492l4.254-12.278a.473.473 0 0 1 .826-.14l8.239 10.273c.325.408-.13.966-.595.724" />
  <path d="M11.89 5.017 6.568 20.583a1.78 1.78 0 0 0 .864 2.155l8.934 4.597a1.79 1.79 0 0 0 2.127-.38l6.752-7.338c.604-.65.632-1.644.075-2.331L14.955 4.469c-.883-1.087-2.61-.77-3.065.548M9.78 16.599l3.316-9.725c.195-.585.966-.715 1.356-.241l6.371 7.876c.53.66-.204 1.57-.966 1.207l-4.383-2.173a.81.81 0 0 0-.929.167c-.678.715-2.09 2.23-3.464 3.697-.576.613-1.598 0-1.32-.79" />
</svg>
`

function redeemAlert(name, title, cost) {
  totalMessages += 1;
  let alertMessage = $.parseHTML(`
    <div class="message-row redeem eventrow followerstyle">
      <div class="anim {msgAlign} {anim}">
       <div class="pfp">
${redeemIc}
</div>
      <div class="redeemcont">
     <span>${name}</span> <span>redeemed</span> <span class="amred">${title}</span> 
      </div>
      </div>
    </div>
  `);


    if (msgAlign === "end") {
            $(alertMessage).appendTo('.main-container').hide();
        }
     else {
            $(alertMessage).prependTo('.main-container').hide();
        } 
      LimitMsg(alertMessage);
}

  function seshUpdateEvent(prevname, newname, title) {
    let text = "", icon = ""
  switch (title) {
    case "topsub":
    text = "new top sub gifter"
    icon = topsbIc;
    break;
    case "topcheer":
    text = "new top all time cheerer"
    icon = topchrIc;
    break;
    case "sessionCheer":
    text = "new top session cheerer"
    icon = topchrIc;
    break;
    case "monthCheer":
    text = "new top month cheerer"
    icon = topchrIc;
    break;
  }

  totalMessages += 1;
let alertMessage = $.parseHTML(BuildSeshItem(prevname, newname, title, "", text, icon));

    if (msgAlign === "end") {
            $(alertMessage).appendTo('.main-container').hide();
        }
     else {
            $(alertMessage).prependTo('.main-container').hide();
        } 
    
    if (!fieldData.minanim) {
        let eventDisplay = $(alertMessage).find(".seshletter").toArray();
        $(alertMessage).find(".name").attr("style", "--ems: " + eventDisplay.length + "em; --pxes: " + eventDisplay.length + "px")
        for (let i = 0; i < eventDisplay.length; i++) {
          if (i == eventDisplay.length - 1) {
            setTimeout(()=>{
              $(alertMessage).find(".seshcont").addClass("pop")
              $(alertMessage).find(".seshcont").removeClass("holdAnim")
            }, 600 + 50 * i)
          }
          setTimeout(()=>{
            $(eventDisplay[i]).addClass("on")
          }, 600 + 50 * i)
         
        }
    } else {
    $(alertMessage).find(".seshcont").addClass("hideprevs");
    }

      LimitMsg(alertMessage)
  }

  let testmsg = null;
  window.addEventListener('onSessionUpdate', async function (obj) {
    if (fieldData.leaderTagsOn || fieldData.topic == "goal") {
    let seshData = obj.detail.session;
    if (leaders.topAlltimeSubGiftUsername.name != seshData["subscriber-alltime-gifter"]["name"].toLowerCase()) {
    seshUpdateEvent(leaders.topAlltimeSubGiftUsername, seshData["subscriber-alltime-gifter"], "topsub")
    leaders.topAlltimeSubGiftUsername.name = seshData["subscriber-alltime-gifter"]["name"].toLowerCase()
    leaders.topAlltimeSubGiftUsername.amount = seshData["subscriber-alltime-gifter"]["amount"]
    }

    if (leaders.topAlltimeCheerUsername.name != seshData["cheer-alltime-top-donator"]["name"].toLowerCase()) {
    seshUpdateEvent(leaders.topAlltimeCheerUsername, seshData["cheer-alltime-top-donator"], "topcheer")
    leaders.topAlltimeCheerUsername.name = seshData["cheer-alltime-top-donator"]["name"].toLowerCase()
    leaders.topAlltimeCheerUsername.amount = seshData["cheer-alltime-top-donator"]["amount"]
    }
    if (leaders.topSessionCheerUsername.name != seshData["cheer-session-top-donator"]["name"].toLowerCase()) {
      seshUpdateEvent(leaders.topSessionCheerUsername, seshData["cheer-session-top-donator"], "sessionCheer")
      leaders.topSessionCheerUsername.name = seshData["cheer-session-top-donator"]["name"].toLowerCase()
      leaders.topSessionCheerUsername.amount = seshData["cheer-session-top-donator"]["amount"]
    }
    if (leaders.topMonthlyCheerUsername.name != seshData["cheer-monthly-top-donator"]["name"].toLowerCase()) {
      seshUpdateEvent(leaders.topMonthlyCheerUsername, seshData["cheer-monthly-top-donator"], "monthCheer")
      leaders.topMonthlyCheerUsername.name = seshData["cheer-monthly-top-donator"]["name"].toLowerCase()
      leaders.topMonthlyCheerUsername.amount = seshData["cheer-monthly-top-donator"]["amount"]
    }

    if (fieldData.topic == "goal") {
      initializeData(seshData)
    }
    }
  })
  window.addEventListener('onEventReceived', async function (obj) {
          if (obj.detail.event.listener === 'widget-button') {         
          let emulated;   
          switch(obj.detail.event.field) {
            case 'testtestMessage':
              emulated = new CustomEvent("onEventReceived", gettestMessage(testmsg, channelName));
              break;
            case "testMessageLong": 
              emulated = new CustomEvent("onEventReceived", testMessageLong(testmsg));
               break;
            case "testMessageVip":
              emulated = new CustomEvent("onEventReceived", testMessageVip(testmsg));
               break;
              case "testMessageSub":
              emulated = new CustomEvent("onEventReceived", testMessageSub(testmsg));
               break;
            case "testMessageMod":
              emulated = new CustomEvent("onEventReceived", testMessageMod(testmsg));
               break;
               case "testMessageFirst":
              emulated = new CustomEvent("onEventReceived", testMessageFirst());
               break;
                case "testSubEvent":
              emulated = new CustomEvent("onEventReceived", testSubEvent(genName()));
               break;
               case "testSubEventNew":
                emulated = new CustomEvent("onEventReceived", testSubEventNew(genName()));
                 break;
                 case "testSubEventGift":
                  emulated = new CustomEvent("onEventReceived", testSubEventGift(genName()));
                break;
               case "testMessageArtist":
                emulated = new CustomEvent("onEventReceived", testMessageArtist(testmsg));
                 break;
               case "testTipEvent":
              emulated = new CustomEvent("onEventReceived", testTipEvent(genName()));
               break;
               case "testCheerEvent":
              emulated = new CustomEvent("onEventReceived", testCheerEvent(genName()));
               break;
               case "testFollowEvent":
              emulated = new CustomEvent("onEventReceived", testFollowEvent(genName()));
               break;
               case "testRaidEvent":
                emulated = new CustomEvent("onEventReceived", testRaidEvent(genName()));
                 break;
               case "testRedeem":
             redeemAlert("milaeshop", "drink water", 50000)
                 break;
            case "test12":
              testSession.detail.session["subscriber-alltime-gifter"]["name"] = genName();
               emulated = new CustomEvent("onSessionUpdate", testSession);
                 break;
             case "commandControlTest":
              emulated = new CustomEvent("onEventReceived", gettestMessage(fieldData.commandControl));
               break;
          }
       if (emulated) window.dispatchEvent(emulated);
          return;
      }
    
    
       
  if (obj.detail.listener === "delete-message") {
        const msgId = obj.detail.event.msgId;
        $(`.message-row[data-msgid=${msgId}]`).remove();
        return;
    } else if (obj.detail.listener === "delete-messages") {
        const sender = obj.detail.event.userId;
        $(`.message-row[data-sender=${sender}]`).remove();
        return;
    }
    
  

    let type = obj.detail.listener;
    let event = obj.detail.event;
   if (fieldData.alertson === true) {
    if (
      type === "subscriber-latest" ||
      type === "tip-latest" ||
      type === "cheer-latest" || 
      type === "follower-latest" || 
      type === "raid-latest"
    ) {
      let alertText = "", alertName = "", alertAmount = "", eventType = "", specialType = "";
      let alertMsg = "";
      if (event.message && fieldData.almsgsOn) {
        alertMsg = `<div class="alertMsg"><svg class="arrow" width="34" height="19" viewBox="0 0 34 19" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M26.146 1.745a1.767 1.767 0 0 0 -2.499 0h0c-0.69 0.69 -0.69 1.809 0 2.499l0.354 -0.354 -0.354 0.354 3.796 3.796H2.885a1.767 1.767 0 0 0 0 3.534h24.558l-3.796 3.796a1.767 1.767 0 1 0 2.499 2.5l6.813 -6.814c0.69 -0.69 0.69 -1.808 0 -2.498z" fill="var(--arrowscol)" stroke="var(--arrowscol)" stroke-linecap="round" stroke-linejoin="round" stroke-width="1"/></svg>
        <span>${event.message}</span></div>`
      }
      let blockToAdd;
      switch (type) {
        case "subscriber-latest":
          if (fieldData.alertssub) {
            if (event.isCommunityGift) {return}
            if (event.bulkGifted == true && event.sender == event.name) {
              alertText = `gifted`;
              alertName = event.sender;
              alertAmount = `${event.amount} ${event.amount == 1 ? "sub" : "subs"}`;
              specialType = event.amount >= subspecial ? "special" : "";
              eventType = "subgift";
              blockToAdd = addGiftBlock(alertName, alertText, alertAmount);
            } else if (event.gifted && event.isCommunityGift !== true) {
              alertText = "gifted a sub";
              alertName = event.sender;
              alertAmount = `1`;
              eventType = "subgift";
              blockToAdd = addGiftBlock(alertName, alertText, alertAmount);
            } else if (
              event.gifted !== true &&
              event.isCommunityGift !== true &&
              event.amount > 1
            ) {
              alertText = `resub`;
              alertName = event.name;
              alertAmount = `X${event.amount}`;
              eventType = "resub";
              blockToAdd = addSubBlock(alertName, alertText, alertAmount);
            } else if (event.gifted !== true && event.isCommunityGift !== true) {
              alertName = event.name;
              alertText = "subscribed";
              eventType = "newsub";
              alertAmount = `NEW`;
              blockToAdd = addNewSubBlock(alertName, alertText, alertAmount);
            } else {
              return;
            }
          }
          break;
        case "tip-latest":
          if (fieldData.alertsdonation) {
           alertText = `tipped`;
           alertName = event.name;
           specialType = event.amount >= tipspecial ? "special" : "";
        
           alertAmount = `${currency}${event.amount.toFixed(2)}`;
           eventType = "tip";
           blockToAdd = addTipBlock(alertName, alertText, alertAmount);
          }
          break;
        case "cheer-latest":
          if (fieldData.alertsbits) {
         alertText = `cheered`;
         alertName = event.name;
         specialType = event.amount >= bitspecial ? "special" : "";
         alertAmount = `${event.amount}`;
         eventType = "cheer";
         blockToAdd = addCheerBlock(alertName, alertText, alertAmount);
          }
          break;
          case "follower-latest": 
          if (fieldData.alertsfollower) {
            alertText = `followed`;
            alertName = event.name;
            eventType = "follower";
            blockToAdd = addFollowerBlock(alertName, alertText);
          }
          break;
          case "raid-latest": 
          if (fieldData.alertraid && event.amount >= minRaid) {
            alertText = `raided with ${event.amount} viewers`;
            alertName = event.name;
            eventType = "raid";
            alertAmount = `${event.amount}`;
            blockToAdd = addRaidBlock(alertName, alertText, alertAmount);
          }
          break;
      }

if (!alertText) return;
totalMessages += 1;
let alertMessage = $.parseHTML(`
    <div class="message-row eventrow ${eventType}style ${specialType}">
      <div class="anim {msgAlign} {anim}">
       ${blockToAdd}
      </div>
    </div>
  `);
  
 if (fieldData.eventmsgsOn) {
  $(alertMessage).find(".alertcont").append(alertMsg);
 }
 
    
    if (msgAlign === "end") {
            $(alertMessage).appendTo('.main-container')
        }
     else {
            $(alertMessage).prependTo('.main-container')
        } 

    $(alertMessage).hide();
      LimitMsg(alertMessage)
   }}
  
    if (obj.detail.listener !== "message") return;
    let data = obj.detail.event.data;

    
         if (data.text.startsWith(fieldData.commandControl)) {
          minimize(data, data.text)
         }
      
        
   
   
       
    
    let username = data.displayName;  
    if (data.text.startsWith("!") && hideCommands === "yes") return;
    if (ignoredUsers.indexOf(data.nick) !== -1) return;
    userType = "default"
    let tags =  obj.detail.event.data.tags;
    let badges = "", badge;
        for (let i = 0; i < data.badges.length; i++) {
        badge = data.badges[i];
        if (badge.type === "artist-badge") {
          userType = "artist";   
      }
        badges += `<div class="${badge.type} custombadge"><img alt="" src="${badge.url}" class="badge2"></div>`;  
    }
    badges = `${badges}`;

    if (tags.subscriber === "1") {userType = "sub"};
    if (tags.mod === "1") {userType = "mod"};
    if (tags.vip === "1") {userType = "vip"};

        for (let i = 0; i < data.badges.length; i++) {
        badge = data.badges[i];
          if (badge.type === "broadcaster") {
            userType = "streamer";   
        }  
    }

    let replyBody = "";
    if (tags["reply-parent-msg-body"] && tags["reply-parent-display-name"]) {
      replyBody = $.parseHTML(`
<svg class="arrow" width="34" height="19" viewBox="0 0 34 19" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M26.146 1.745a1.767 1.767 0 0 0 -2.499 0h0c-0.69 0.69 -0.69 1.809 0 2.499l0.354 -0.354 -0.354 0.354 3.796 3.796H2.885a1.767 1.767 0 0 0 0 3.534h24.558l-3.796 3.796a1.767 1.767 0 1 0 2.499 2.5l6.813 -6.814c0.69 -0.69 0.69 -1.808 0 -2.498z" fill="var(--arrowscol)" stroke="var(--arrowscol)" stroke-linecap="round" stroke-linejoin="round" stroke-width="1"/></svg>
<span class="replybod"><span class="toName">${tags["reply-parent-display-name"] + ":" + "&nbsp"}</span><span class="toMessage">${tags["reply-parent-msg-body"].replace(/\\s/g, ' ')}</span></span>`)
    }
    
    
    let leaderBody = "";
    let classToAdd = "";
    
    if (fieldData.leaderTagsOn) {

    if (data.nick.toLowerCase() == leaders.topSessionCheerUsername.name.toLowerCase()) {
      classToAdd = "topcheerstyle topstyle";
      leaderBody = leaderBuild(`<div><svg class="modside topchr" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 12.57 15.51">
  <path d="M5.16.6.14 9.95c-.27.5-.13 1.12.32 1.46l5.2 3.87c.41.31.98.3 1.39-.02l5.07-3.96c.45-.35.58-.98.29-1.48L7.17.58c-.45-.79-1.58-.77-2.01.03"/>
</svg></div>STREAM LEADER`)
    }
   if (data.nick.toLowerCase() == leaders.topMonthlyCheerUsername.name.toLowerCase()) {    
      classToAdd = "topcheerstyle topstyle";
      leaderBody = leaderBuild(`<div><svg class="modside topchr" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 12.57 15.51">
  <path d="M5.16.6.14 9.95c-.27.5-.13 1.12.32 1.46l5.2 3.87c.41.31.98.3 1.39-.02l5.07-3.96c.45-.35.58-.98.29-1.48L7.17.58c-.45-.79-1.58-.77-2.01.03"/>
</svg></div>MONTH LEADER`)
    }
    if (data.nick.toLowerCase() == leaders.topAlltimeCheerUsername.name.toLowerCase()) {
      classToAdd = "alltimetop topcheerstyle topstyle";
      leaderBody = leaderBuild(`<div><svg class="modside topchr" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 12.57 15.51">
  <path d="M5.16.6.14 9.95c-.27.5-.13 1.12.32 1.46l5.2 3.87c.41.31.98.3 1.39-.02l5.07-3.96c.45-.35.58-.98.29-1.48L7.17.58c-.45-.79-1.58-.77-2.01.03"/>
</svg>
</div>ALL TIME LEADER`)
    }
    if (data.nick.toLowerCase() == leaders.topAlltimeSubGiftUsername.name.toLowerCase()) {
      classToAdd = "topgiftstyle topstyle";
      leaderBody = leaderBuild(`<div><svg class="topsub1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 12.4 9.56">
  <path d="M12.4 1.93a.4.4 0 0 0-.08-.31.403.403 0 0 0-.57-.08L9.4 3.3s-.02.01-.03.02c-.26.17-.61.1-.78-.16L6.64.23a.518.518 0 0 0-.87 0L3.81 3.16a.56.56 0 0 1-.8.14L.65 1.54a.43.43 0 0 0-.31-.08c-.22.03-.38.24-.34.47.25 1.64.5 5.71.76 7.35h.09c.1.16.27.28.48.28h9.75c.2 0 .38-.12.48-.28h.09c.25-1.64.5-5.71.75-7.34Z"/>
</svg></div>
 SUB GIFT KING`)
    }
     }
   data.emotes = emotesStorage.concat(data.emotes);  

    let message = msgDiv(data);
    let findUsername = message.split(" "); 
    findUsername = findUsername.map(element => {
      if (element.startsWith("@")) {
        return `<span class="mentionNick">${element}</span>`;
      }
      return element;
    });
       message = findUsername.join(" ");
   
    let pronounsDiv = `<span class="pronouns"></span>`;
 
    addMessage(username, badges, message, data.userId, data.msgId, userType, emoteOnly, replyBody, classToAdd, leaderBody);

let currDiv = $(`.message-row[data-msgid=${data.msgId}]`);
if (fieldData.pfptype == "pfpTwitch" && !(userType == "default" && fieldData["pfp-subonly"])) {
let chatterClass = "id" + data.userId;
let pfpDiv = $(`.${chatterClass}`)
   getPicture(data.nick, $(pfpDiv), chatterClass);
  }

let pronounsText = "";
  let pronounsEl;
  if (pronounsOn) {
  async function getP() {
    pronounsText = await getUserPronoun(data.displayName);
    if (pronounsText) {
      pronounsEl = ``
    $(currDiv).find(".pronouns").text(`${pronounsText} `).addClass("pronounsDiv");
    }}
    getP();
  }
});

function initializeData(seshData) {
	switch (fieldData["goalType"]) {
		default:
		case "tip":
		case "cheer":
			sum = +seshData[`${fieldData.goalType}-${fieldData.timeframe}`]["amount"];
		break;
		case "follower":
		case "subscriber":
			sum = +seshData[`${fieldData.goalType}-${fieldData.timeframe}`][`${fieldData.timeframe == "goal" ? "amount" : "count"}`];
		break;
    case "sub-points":
    sum = +seshData[`subscriber-points`]["amount"];
     break;
	}

  let goalNums = `${sum}/${goal}`
  $(".goalD span").html(goalNums)
}




window.addEventListener('onWidgetLoad', async obj => {

//  $(".wrap").css("height", window.innerHeight - 5 + "px");
  fieldData = obj.detail.fieldData;
  const seshData = obj.detail.session.data;
  testSession = {detail: {session: seshData}}
  if (fieldData.useTesttext & fieldData.testText !== "") testmsg = fieldData.testText;
  currency = obj.detail.currency.symbol;
  channelName = obj.detail.channel.username;
  providerID = obj.detail.channel.providerId;
  
  ({hideCommands, msgAlign, msgHideOpt, pronounsOn, largeEmotes, msgLimit, msgLimitAmount, badgesDisplay, badgesCustom, msgConnect} = fieldData);
  if (!largeEmotes) fieldData.stickerEmote = false;
  
  leaders.topAlltimeSubGiftUsername.name = seshData["subscriber-alltime-gifter"]["name"].toLowerCase();
  leaders.topAlltimeSubGiftUsername.amount = seshData["subscriber-alltime-gifter"]["amount"];
  leaders.topAlltimeCheerUsername.name = seshData["cheer-alltime-top-donator"]["name"].toLowerCase();
  leaders.topAlltimeCheerUsername.amount = seshData["cheer-alltime-top-donator"]["amount"] ;
  leaders.topSessionCheerUsername.name = seshData["cheer-session-top-donator"]["name"].toLowerCase();
  leaders.topSessionCheerUsername.amount = seshData["cheer-session-top-donator"]["amount"];
  leaders.topMonthlyCheerUsername.name = seshData["cheer-monthly-top-donator"]["name"].toLowerCase();
  leaders.topMonthlyCheerUsername.amount = seshData["cheer-monthly-top-donator"]["amount"];
  
  timechange = fieldData.time;
  
 
  if (msgAlign === "end") {
    $(".main-container").css("justify-content", "flex-end");
  }
  if (msgAlign === "top") {
    $(".main-container").css("justify-content", "flex-start");
  }

  bitspecial = fieldData.bitspecial;
  subspecial = fieldData.subspecial;
  tipspecial = fieldData.tipspecial;

  if (fieldData.namebgon) {
    $(".main-container").addClass("namebgon");
  }
  if (fieldData.lastEmote) {
    $(".footer").addClass("lastEmoteOn");
  } else {
  $(".lastEmote").remove();
  }
  if (!fieldData.footerOn) {
     $(".footerwrap").remove();
  }
  
  if (fieldData.alertsRight) {
    $(".main-container").addClass("alertsRight");
  }
  if (fieldData.square) {
    $("body").css("--brdr", "0px");
  }
  

  if (!fieldData.viewercount) {
    $(".odometer").remove()
  } else {
      let timeToRefresh = 60;
      getData();
      setInterval(function () {
          getData();
      }, timeToRefresh * 1000);
  }
  
  
  
    if (fieldData.minanim) {
   $(".main-container").addClass("nosmooth minanim");
   fieldData.typewritenames = false;
}
  
  
  if (fieldData.minals) {
    $(".main-container").addClass("minals");
  }
  if (fieldData.gradName) {
    $(".main-container").addClass("gradName");
  }
  if (fieldData.pfptype == "none" || fieldData.hidepfp) {
    $(".main-container").addClass("pfpoff");
  } else {
    $(".main-container").addClass("pfpon");
  }
  if (!fieldData.msgbgoff) {
    $(".main-container").addClass("msgbgoff");
  } else {
    $(".main-container").addClass("msgbgon");
  }
  
  if (fieldData.eventbgoff) {
    $(".main-container").addClass("eventbgoff minals");
  }
  
    if (!fieldData.smooth) {
  $(".main-container").addClass("nosmooth");
}
  
  goalTitle = fieldData.goalT;
  goal = fieldData.goalTarget;
  
  if (fieldData.topic == "goal") { 
    $(".topic").html(`<div class="goalTitle"><span>${goalTitle}</span></div>
      <svg class="arrow" width="34" height="19" viewBox="0 0 34 19" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M26.146 1.745a1.767 1.767 0 0 0 -2.499 0h0c-0.69 0.69 -0.69 1.809 0 2.499l0.354 -0.354 -0.354 0.354 3.796 3.796H2.885a1.767 1.767 0 0 0 0 3.534h24.558l-3.796 3.796a1.767 1.767 0 1 0 2.499 2.5l6.813 -6.814c0.69 -0.69 0.69 -1.808 0 -2.498z" fill="var(--arrowscol)" stroke="var(--arrowscol)" stroke-linecap="round" stroke-linejoin="round" stroke-width="1"/></svg>
     <div class="goalD"><span></span></div>`)
     initializeData(seshData)
  } else if (fieldData.topic == "text") {
    $(".topic").html(`<div class="goalTitle"><span>${fieldData.topicText}</span></div>`);
  } else if (fieldData.topic == "socials") {
    $(".topic").html(`
      <div class="alerttextwrap"></div>
     `)
  }

  if (fieldData.userTyping) {
    let Typing = `<div class="userTyping">
<div class="typingText"></div></div>`
$(Typing).appendTo(".win")
    } 
  
   if (fieldData.msgFade === true) {
     if (msgAlign === "end") {
      $('body').toggleClass("out");
    } else {
      $('body').toggleClass("outdown");
    }
  }

  if (fieldData.topic == "socials") {
  let items = [];
  for (let i = 1; i < 7; i++) {
    let item = fieldData['socialsslot' + i];
    if (item != "none") {
      items.push([fieldData['socialsslot' + i + "name"], socialsIcons[`${item}`]])
    }        
  }

  function updateSocials() {
 //     $(".alerttextwrap").addClass("off hidee");
 //  $(".iconwrap").html(items[counter][1]) 
 $(".alerttextwrap").fadeOut(400)
      setTimeout(()=>{
  $(".alerttextwrap").html(`<div class="iconwrap">${items[counter][1]}</div>
    <svg class="arrow" width="34" height="19" viewBox="0 0 34 19" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M26.146 1.745a1.767 1.767 0 0 0 -2.499 0h0c-0.69 0.69 -0.69 1.809 0 2.499l0.354 -0.354 -0.354 0.354 3.796 3.796H2.885a1.767 1.767 0 0 0 0 3.534h24.558l-3.796 3.796a1.767 1.767 0 1 0 2.499 2.5l6.813 -6.814c0.69 -0.69 0.69 -1.808 0 -2.498z" fill="var(--arrowscol)" stroke="var(--arrowscol)" stroke-linecap="round" stroke-linejoin="round" stroke-width="1"/></svg>
    <span>${items[counter][0]}</span>`) 
    $(".alerttextwrap").fadeIn(400)
        }, 500) 
        
  }
  updateSocials()
    setInterval(() => {
      counter++;
      if (counter >= items.length) counter = 0;
      updateSocials()
    }, timechange * 1000)
  }

  
  let fontname1 = fieldData.msgFont.split(" ").join("+");
  let font = document.createElement("style");
  $(font).html(`<style>
  @import url('https://fonts.googleapis.com/css2?family=${fontname1}:wght@300;400;500;600;700;800;900&display=swap');
</style>`).prependTo($('body'));  

   ignoredUsers = fieldData.ignoredUsers.toLowerCase().replace(" ", "").split(",");
  if (fieldData.editsMode1) {
   $(".wrap").css({"--asdbg": "var(--bgframe)", 
                  "--asdbg2": "var(--msgbg)"})
  }
 
if (fieldData.alertpoints) {
  const socket = new WebSocket('wss://pubsub-edge.twitch.tv')
  const eventTopic = `community-points-channel-v1.${providerID}`

  socket.onopen = (event) => {
    const info = {
      "type": "LISTEN",
      "data": {
        "topics": [eventTopic]
      }
    }
    socket.send(JSON.stringify(info));
    
    setInterval( () => { sendPing() }, 120000)
  }
  
 
  socket.onmessage = (event) => {
    const data = JSON.parse(event.data);
    
    if(event.data.type == "PING"){      
      sendPong();
    }

    if(data.data?.topic == eventTopic){
      const redemptionData = JSON.parse(data.data.message);
      
      if(redemptionData.type == 'reward-redeemed'){
        const redUser = redemptionData.data.redemption.user["display_name"]
        const redTitle = redemptionData.data.redemption.reward.title
        const redCost = redemptionData.data.redemption.reward.cost
        if (redCost >= fieldData.redeemShow) redeemAlert(redUser, redTitle, redCost)
        
      }
    }
  }

  function sendPing(){
    socket.send(JSON.stringify( { type: "PING" } ));
  }
   
  function sendPong(){
    socket.send(JSON.stringify( { type: "PONG" } ));
  }
}


  if (pronounsOn) { await getPronouns() };
if (fieldData.EmotesAPI) {
  await getEmotes()
}

    await getTwitchAuthorization();
   if (fieldData.editsMode) {
     leaders.topMonthlyCheerUsername["name"] = "playapex"
 //   window.dispatchEvent(new CustomEvent("onEventReceived", gettestMessage(testmsg, channelName)));
      window.dispatchEvent(new CustomEvent("onEventReceived", testMessageFirst()));
    window.dispatchEvent(new CustomEvent("onEventReceived", testMessageLong(testmsg)));
    window.dispatchEvent(new CustomEvent("onEventReceived", testMessageVip(testmsg)));
    window.dispatchEvent(new CustomEvent("onEventReceived", testMessageMod(testmsg)));
    window.dispatchEvent(new CustomEvent("onEventReceived", testMessageSub(testmsg)));
    window.dispatchEvent(new CustomEvent("onEventReceived", testMessageArtist(testmsg)));
    
  // 
 //   window.dispatchEvent(new CustomEvent("onEventReceived", testSubEvent(genName())));
     
    /*     let o = 0, iu = 1000;
  let delmsg = 0.8, delalert = 1.1;
     fieldData.minimalal = true;
   setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", gettestMessage()));
   }, iu + o * 1000)
   o += delmsg;
   setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageVip()));
   }, iu + o * 1000)
   o += delmsg;
   setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testCheerEvent));
   }, iu + o * 1000)
   o += delalert; 
   setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testFollowEvent));
   }, iu + o * 1000)
   o += delalert;
     setTimeout(()=> {
       fieldData.minimalal = true;
   window.dispatchEvent(new CustomEvent("onEventReceived", testSubEvent));
   }, iu + o * 1000)
   o += delalert;
   setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageFirst()));
   }, iu + o * 1000)
   o += delmsg;
     setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageFirst()));
   }, iu + o * 1000)
   o += delmsg;
    setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", gettestMessage()));
   }, iu + o * 1000)
   o += delmsg;
    setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageLong()));
   }, iu + o * 1000)
   o += 0.8;
    setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageVip()));
   }, iu + o * 1000)
   o += 0.8;
     setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageMod()));
   }, iu + o * 1000)
   o += 0.8;
     setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageSub()));
   }, iu + o * 1000)
   o += 0.8;
     setTimeout(()=> {
   window.dispatchEvent(new CustomEvent("onEventReceived", testMessageFirst()));
   }, iu + o * 1000)
   o += 0.8;
   setTimeout(()=> {
       fieldData.minimalal = true;
   window.dispatchEvent(new CustomEvent("onEventReceived", testSubEvent));
   }, iu + o * 1000)
   o += delalert;
     */
   }

});

function msgDiv(message) {
   let hehecount = 0;
  let text = html_encode(message.text);
  let data = message.emotes; 
  let temparr = [];
  data.forEach(el => temparr.push(el.name))
  let textsolid = text.split(" ");
  const emotesarr = textsolid.filter(value => temparr.includes(value))
  let notext = text.replace(/\p{C}/gu, '').trim();
  for (let i = 0; i < data.length; i++) {
    let emoteName = data[i]["name"];
    let regex = new RegExp(`\\b${emoteName}\\b`, "g"); 
    notext = notext.replace(regex, " ").replace(/\p{C}/gu, '').trim()
  }

    notext.trim() === "" ? emoteOnly = true : emoteOnly = false;



  return text
      .replace(
          /([^\s]*)/gi,
          function (m, key) {
              let result = data.filter(emote => {
                  return html_encode(emote.name) === key
              });
              let count = 0;
              if (typeof result[0] !== "undefined") {
                let emote;
                count = emotesarr.length;    
                if (notext.trim() === "" && largeEmotes) {
                  $(".lastEmote").html(`<img class="sclup" src="${result[0]['urls'][2]}"/>`)
                if (count === 1) {
                  let url = result[0]['urls'][4];
                  if (url.search(/cdn.frankerfacez.com/ !== -1)) {
                  url = url.replace("https:https:", "https:");
                  }
                  emote = `<img class="emote large" src="${url}"/>`
     
                } else if (count > 1) {         
                  let url = result[0]['urls'][2];
                  if (url.search(/cdn.frankerfacez.com/ !== -1)) {
                  url = url.replace("https:https:", "https:");
                  }
                  emote = `<img class="emote default" src="${url}"/>`;
                } 
              } else {
                let url = result[0]['urls'][1];
                if (url.search(/cdn.frankerfacez.com/ !== -1)) {
                  url = url.replace("https:https:", "https:");
                  }
                emote = `<img class="emote nolarge" src="${url}"/>`;
                } 
                return emote;
          } else {
            return key
          };
        }
      );
}


function html_encode(e) {
    return e.replace(/[<>"^]/g, function (e) {
        return "&#" + e.charCodeAt(0) + ";";
    });
}
function gettestMessage(testmsg, channelName) {
  return {
      detail: {
          listener: "message",
          event: {
              data: {
                  tags: {
                      badges: "moderator/1,partner/1",
                      color: "#1e90ff",
                      mod: "1",
                      subscriber: "1",
                      "user-id": "100135114",
                      "user-type": "mod"
                  },
                  userId: "100135114",
                  displayName: channelName,
                  nick: channelName,
                  displayColor: "#5B99FF",
                  badges: [{
                      "type": "broadcaster",
                      "version": "1",
                      "url": "https://static-cdn.jtvnw.net/badges/v1/5527c58c-fb7d-422d-b71b-f309dcb85cc1/3"
                  }],
                  text: `${testmsg ? testmsg : "This is a test message"}`,
                  emotes: [],
                  msgId: `85909-412c-4eee-b80d-89123f72ba${randNum()}4`
              },
              renderedText: 'Test message in a custom chat'
          }
      }
  }
}

function testMessageLong(testmsg) {
  return {
      detail: {
          listener: "message",
          event: {
              data: {
                  tags: {
                      badges: "",
                      color: "#8a2be2",
                      mod: "0",
                      subscriber: "0",
                      "user-id": "100135115",
                      "user-type": "mod"
                  },
                  userId: "100135115",
                  displayName: "Follower user",
                  nick: "riotgames",
                  displayColor: "#8a2be2",
                  badges: [],
                  text: `${testmsg ? testmsg : "This is a viewer message. Long long long long long long long long long long long long long long long long message."}`,
                  emotes: [],
                  msgId: `43285909-412c-4eee-b80d-83452ba${randNum()}3`
              },
              renderedText: 'Test message in a custom chat'
          }
      }
  }
}
function testMessageSub(testmsg) {
  return {
      detail: {
          listener: "message",
          event: {
              data: {
                  tags: {
                      badges: "subscriber/1",
                      color: "#ff69b4",
                      vip: "0",
                      subscriber: "1",
                      "user-id": "100135116",
                      "user-type": "subscriber",
                      "reply-parent-display-name": "moderator",
                      "reply-parent-msg-body": "This is moderator message"
                  },
                  userId: "100135116",
                  displayName: "Subscriber",
                  nick: "CapcomUSA",
                  displayColor: "#ff69b4",
                  badges: [{
                      type: "partner",
                      version: "1",
                      url: "https://static-cdn.jtvnw.net/badges/v1/d12a2e27-16f6-41d0-ab77-b780518f00a3/3",
                      description: "Verified"
                  }],
                  text: `${testmsg ? testmsg : "hey @moderator, I am a sub"}`,
                  emotes: [],
                  msgId: `285909-412c-4eee-b80d-89f1482ba${randNum()}2`
              },
              renderedText: 'Test message in a custom chat'
          }
      }
  }
}

function testMessageVip(testmsg, name) {
  return {
      detail: {
          listener: "message",
          event: {
              data: {
                  tags: {
                      badges: "vip/1",
                      color: "#ff69b4",
                      vip: "1",
                      subscriber: "0",
                      "user-id": "100135117",
                      "user-type": "vip"
                  },
                  userId: "100135117",
                  displayName: "Vip user",
                  nick: `${name ? name : "playapex"}`,
                  displayColor: "#ff69b4",
                  badges: [{
                      type: "vip",
                      version: "1",
                      url: "https://static-cdn.jtvnw.net/badges/v1/b817aba4-fad8-49e2-b88a-7cc744dfa6ec/3"
                  }],
                  text: `${testmsg ? testmsg : "This is a VIP user test message"}`,
                  emotes: [],
                  msgId: `285909-412c-4eee-b80d-89f1482ba${randNum()}1`
              },
              renderedText: 'Test message in a custom chat'
          }
      }
  }
}

function testMessageMod(testmsg) {
  return {
      detail: {
          listener: "message",
          event: {
              data: {
                  tags: {
                      badges: "moderator/1",
                      color: "#00ff7f",
                      mod: "1",
                      subscriber: "1",
                      "user-id": "100135118",
                      "user-type": "mod"
                  },
                  userId: "100135118",
                  displayName: "Moderator",
                  nick: "cdprojektred",
                  displayColor: "#00ff7f",
                  badges: [{
                      type: "moderator",
                      version: "1",
                      url: "https://static-cdn.jtvnw.net/badges/v1/3267646d-33f0-4b17-b3df-f923a41db1d0/3",
                      description: "Moderator"
                  }],
                  text: `${testmsg ? testmsg : "This is a moderator test message"}`,
                  emotes: [],
                  msgId: `43285909-412c-4eee-b80d-89228ba${randNum()}0`
              },
              renderedText: 'Test message in a custom chat'
          }
      }
  }
}
              function testMessageFirst() {
                 counterEmotes++
      counterEmotes = counterEmotes > 2 ? 0 : counterEmotes;
                let emotesText, emotes;
                switch (counterEmotes) {
                case 2:
                emotes = `{ "type": "twitch","name": "PepeLaugh","id": "112291","gif": false,"animated": false,"urls": {"1": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/1x.avif","2": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/2x.avif","4": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/4x.avif"},"start": 0,"end": 7}, { "type": "twitch","name": "PepeLaugh","id": "112291","gif": false,"animated": false,"urls": {"1": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/1x.avif","2": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/2x.avif","4": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/4x.avif"},"start": 0,"end": 7}, { "type": "twitch","name": "PepeLaugh","id": "112291","gif": false,"animated": false,"urls": {"1": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/1x.avif","2": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/2x.avif","4": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/4x.avif"},"start": 0,"end": 7}, { "type": "twitch","name": "PepeLaugh","id": "112291","gif": false,"animated": false,"urls": {"1": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/1x.avif","2": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/2x.avif","4": "https://cdn.7tv.app/emote/60afbb3952a13d1adb34b2a1/4x.avif"},"start": 0,"end": 7}`
 emotesText = "PepeLaugh  PepeLaugh  PepeLaugh  PepeLaugh  󠀀"
                break;
                case 1:
emotes = `{ "type": "twitch","name": "CatBag","id": "112291","gif": false,"animated": false,"urls": {"1": "https://cdn.frankerfacez.com/emote/25927/1","2": "https://cdn.frankerfacez.com/emote/25927/2","4": "https://cdn.frankerfacez.com/emote/25927/4"},"start": 0,"end": 7}`
 emotesText = " CatBag "
               break;
               case 0:
emotes = `{ "type": "twitch","name": "Binoculous","id": "112291","gif": false,"animated": false,"urls": {"1": "https://cdn.7tv.app/emote/62348f3b73f35ccbda40810c/1x.webp","2": "https://cdn.7tv.app/emote/62348f3b73f35ccbda40810c/2x.webp","4": "https://cdn.7tv.app/emote/62348f3b73f35ccbda40810c/4x.webp"},"start": 0,"end": 7}`
emotesText = " Binoculous "
               break;
         }
let obj = `{
  "detail": {
    "listener": "message",
    "event": {
      "data": {
        "tags": {
          "badges": "",
          "color": "#b22222",
          "first-msg": "1",
          "userId": "100998119"
        },
        "userId": "100995119",
        "displayName": "Hehehaha",
		"nick": "Hehehaha",
        "displayColor": "#b22222",
        "badges": [],
        "text": "${emotesText}",
        "emotes": [
          ${emotes}
        ],
        "msgId": "43285909-412c-4eee-b80d-89228ba${randNum()}0"
      }
    }
  }
}`

                return JSON.parse(obj);
            }

 async function get(URL) {
  return await fetch(URL)
    .then(async res => {
      if (!res.ok) return null
      return res.json()
    })
    .catch(error => null)
}

 async function getUserPronoun(username) {
  const lowercaseUsername = username.toLowerCase()
  let pronouns = pronounsCache[lowercaseUsername]
  if (!pronouns || pronouns.expire < Date.now()) {
    const res = await get(PRONOUNS_API.user(lowercaseUsername))
    const [newPronouns] = res
    pronounsCache[lowercaseUsername] = {
      ...newPronouns,
      expire: Date.now() + 1000 * 60 * 5, 
    }
    pronouns = pronounsCache[lowercaseUsername]
  }

  if (!pronouns.pronoun_id) {
    return null
  }
  return pronounsObj.pronouns[pronouns.pronoun_id];
}

function testMessageArtist(testmsg) {
  return {
      detail: {
          listener: "message",
          event: {
              data: {
                  tags: {
                      badges: "",
                      color: "#8a2be2",
                      mod: "0",
                      subscriber: "0",
                      "user-id": "100135115",
                      "user-type": "mod"
                  },
                  userId: "100135115",
                  displayName: "Artist",
                  nick: "Milaeshop",
                  badges: [{
                                            "type": "artist-badge",
                                            "version": "1",
                                            "url": "https://static-cdn.jtvnw.net/badges/v1/4300a897-03dc-4e83-8c0e-c332fee7057f/3",
                                            "description": "Artist"
              }],
                  text: `${testmsg ? testmsg : "This is an artist message"}`,
                  emotes: [],
                  msgId: `43285909-412c-4eee-b80d-83452ba${randNum()}3`
              },
              renderedText: 'Test message in a custom chat'
          }
      }
  }
}

function testSubEventNew(usrname) {
  return {detail: {
      listener: "subscriber-latest",
      event: {
          name: usrname,
          tier: "3000",
          amount: `1`,
          message: `Hi, I just resubscribed! Love you streamer`
      },
  }
}}

function testSubEventGift(usrname) {
  return {detail: {
      listener: "subscriber-latest",
      event: {
          name: usrname,
          sender: usrname,
          tier: "3000",
          amount: `40`,
          bulkGifted: true
      },
  }
}}

function testSubEvent(usrname) {
  return {detail: {
                    listener: "subscriber-latest", event: {
                            name: usrname,
                            tier: "3000",
                            amount: `10`,
                            message: `Hi, I just resubscribed! Love you streamer`
                        },
                    }
                 }
                }

function testCheerEvent(usrname) {
  return {detail: {
                    listener: "cheer-latest", event: {
                            name: usrname,
                            amount: `10000`,
                            message: `Cheers for streamer Kappa Cheers for streamer Kappa Cheers for streamer Kappa Cheers for streamer Kappa Cheers for streamer Kappa `
                        },
                    }
                 }}

  function testFollowEvent(usrname) {
return {detail: {
                    listener: "follower-latest", event: {
                            name: usrname
                        },
                    }
                 }
                }

function testTipEvent(usrname) {
  return {
    detail: {
         listener: "tip-latest", event: {
           name: usrname,
              tier: "3000",
          amount: 500,
                  message: `Tip for the streamer and alert message added to the tip ho-ho ha-ha`
                        },
                    }
                 }
                }

 function testRaidEvent(usrname) {
  return {
    detail: {
  listener: "raid-latest", event: {
          name: usrname, 
          amount: 500
      },
  }
}
}


  function randNum() {
    return Math.floor(Math.random() * 99999);
     }

     var nameList = [
      'Judah', 'Alejandro', 'Roberto', 'Fernando',
      'Paparazzi', 'YourBiggestFan', "Monster", "BloodyMary", "i_m_kinda_busy"
    ];
    
    function genName() {
      return nameList[Math.floor(Math.random() * nameList.length)];
    }
    

      async function getEmotes() {
        const res = await get(`https://7tv.io/v3/users/twitch/${providerID}?timestamp=${new Date().getTime()}`);
        let emotes = res["emote_set"]["emotes"];
       for (let i = 0; i < emotes.length; i++) {
        let emote = {name: emotes[i]["name"], urls: {1: "https:" + emotes[i]["data"]["host"]["url"] + "/" + emotes[i]["data"]["host"]["files"][1]["name"],
                                              2: "https:" + emotes[i]["data"]["host"]["url"] + "/" + emotes[i]["data"]["host"]["files"][2]["name"],     
                                              4: "https:" + emotes[i]["data"]["host"]["url"] + "/" + emotes[i]["data"]["host"]["files"][3]["name"]}} 
        emotesStorage.unshift(emote);
        }
       }


       function LimitMsg(el) {
    if (fieldData.typewritenames) {
          let eventDisplay = $(el).find(".eventletter").toArray();
          if (eventDisplay.length) {
          $(el).find(".name").attr("style", "--ems: " + eventDisplay.length + "em; --pxes: " + eventDisplay.length + "px")
    
            for (let i = 0; i < eventDisplay.length; i++) {
              setTimeout(()=>{
                $(eventDisplay[i]).addClass("eventletterUp")
              }, 100 + 50 * i)
             
            }}
        }

        if (fieldData.smooth && !document.hidden) {
          $(el).slideToggle(200);
          el = null;
             } else {
             $(el).show();
             el = null;
             }

        const limit = msgLimit ? msgLimitAmount : 15;
if (msgAlign === "end") {
    $('.main-container').children().slice(0, -limit).fadeOut(200, function() {
        $(this).remove();
    });
} else {
    $('.main-container').children().slice(limit).fadeOut(200, function() {
        $(this).remove();
    });
}
      }

 function minimize(data, text) {
       const {nick, tags, channel} = data;
            const userstate = {
                'mod': parseInt(tags.mod),
                'badges': {
                    'broadcaster': (nick === channel),
                }
            };
            if (!(userstate.mod && fieldData['managePermissions'] === 'mods' || userstate.badges.broadcaster || fieldData.additionalUsers.includes(nick.toLowerCase()))) return;
            let heightDynamic = parseInt(text.split(' ')[1])
            if (isNaN(heightDynamic)) {
               if (Math.round($(".wrap").innerHeight()) < Math.round(window.innerHeight - 5)) {
                 if (!document.hidden) {
                  $(".wrap").animate({height: window.innerHeight - 5}, 300)
                 } else {
                 $(".wrap").css({height: window.innerHeight - 5})
                 }
               } else {
                  if (!document.hidden) {
               $(".wrap").animate({height: fieldData.minimizeHeight}, 300)
                  } else {
                   $(".wrap").css({height: fieldData.minimizeHeight})
                  }
               }
            } else {
              if (heightDynamic > window.innerHeight) heightDynamic = Math.round(window.innerHeight - 5);
                 $(".wrap").animate({height: heightDynamic}, 300)
            }           
       }


      let icons = getRoleIcs();

      async function getPicture(nick, el, chatterClass) {
        const endpoint = `https://api.twitch.tv/helix/users?login=${nick}`;
        let authorizationObject = dataD;
        let { access_token, expires_in, token_type } = authorizationObject;
        token_type =
        token_type.substring(0, 1).toUpperCase() +
        token_type.substring(1, token_type.length);
        let authorization = `${token_type} ${access_token}`;
        let headers = {
        authorization,
        "Client-Id": clinetId,
        };
        fetch(endpoint, {
        headers,
        })
        .then((res) => res.json())
        .then((data) => uploadPictues(data, el, chatterClass));
      }
      
      function uploadPictues(data, el, chatterClass) {  
      let userObj = JSON.stringify(data);
      userObj = JSON.parse(userObj);
      let image1 = userObj.data[0]["profile_image_url"];
      $(`.${chatterClass}`).css("background-image", `url("${image1}")`);
          if (!userImageLoaded[chatterClass]) {
        let styleSheet = document.createElement("style");
      $(styleSheet).html(`<style>
      .${chatterClass} { background-image: url("${image1}") }
      </style>`)
      $(styleSheet).prependTo($('body'));   
        }
        userImageLoaded[chatterClass] = true;
      }  

    function getData() {
      $.get("https://decapi.me/twitch/viewercount/" + channelName, function (data) {
          if (data && !isNaN(data)) {
       
          $(".odometer span").html(data);    
      } else {
          $(".odometer span").html("0");    
      }
      });
    }

      async function getTwitchAuthorization() {
        let url = `https://id.twitch.tv/oauth2/token?client_id=${clinetId}&client_secret=${clinetSecret}&grant_type=client_credentials`;
        return fetch(url, {
        method: "POST",
        })
        .then((res) => res.json())
        .then((data) => {
           dataD = data;
          
            return;
        });
    }

