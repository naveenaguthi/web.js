const puppeter=require("puppeteer");
let cpage;
console.log("Before");
const browserOpenpromise=puppeter.launch({
    headless:false,
    slowMo:true,
    defaultViewport:null,
});
browserOpenpromise
   .then(function(browser){
       const pageArrpromise=browser.pages();
       return pageArrpromise;
   }).then(function(browserPages){
       page=browserPages[0];
       let gotoPromise=page.goto("https://www.google.com/");
       return gotoPromise;
   }).then(function(){
       let elementWaitPromise=page.waitForSelector("input[type='text']',{visible:true});
       return elementWaitPromise;
   }).then(function(){
       let keysWillBeSendPromise=page.type("input[type='text']",wikkipedia);
       return keysWillBeSendPromise;
   }).then(function(){
       let enterWillBePressed=page.keyboard("Enter);
       return entewrWillBePressed;
   }).then(function(){
       let elementWaitPromise=page.waitForSelector("<h3 class="LC20lb MBeuO DKV0Md">Wikipedia</h3>");
       return elementWaitPromise;
   }).then(function(){
       let elementWaitPromise=page.waitForSelector("<strong>English</strong>");
       return elementWaitPromise;
   }).then(function(){
       let elementWaitPromise=page.waitForSelector("<a href="/wiki/Wikipedia:Contents/Portals" title="Wikipedia:Contents/Portals">All portals</a>");
       return elementWaitPromise;

   }).then(function(){
        let elementWaitPromise=page.waitForSelector("<a href="/wiki/Wikipedia:Contents/A%E2%80%93Z_index" title="Wikipedia:Contents/A–Z index">A–Z index</a>");
        return elementWaitPromise;
   }).then(function(){
       let elementWaitPromise=page.waitForSelector("<a href="/wiki/Special:AllPages/N" title="Special:AllPages/N">N</a>");
        return elementWaitPromise;
   }).then(function(){
        let elementWaitPromise=page.waitForSelector)("<a href="/wiki/N" title="N">N</a>");
        return elementWaitPromise;
   }).then(function(){
        let elementWaitPromise=page.waitForSelector("<span class="toctext">History</span>");
        return elementWaitPromise;
   }).then(function(){
        let elementWaitPromise=page.waitForSelector("<span class="toctext">Use in writing systems</span>");
        return elementWaitPromise;
   }).then(function(){
        let elementWaitPromise=page.waitForSelector("<span class="toctext">Other uses</span>");
        return elementWaitPromise;
   })
