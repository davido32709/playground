# author: Dawid Piechowka
## Project: web simple game
### 2a SCI TI

Functionalities:
*loading screen before game
*protection against accidental closing or overloading
*player as img
*cookie accept
    *platforms on html canvas     
    *player's control by arrows and WASD
    *player reacts for platforms
    *fall animation and menu
    *menu bar half transparent like here https://musicfy.lol/
    *parallax platfroms looped
    *hq player mechanics movement, move's accelerating mulitplied by time key pressed
    *parallax background, three hues of gray stripes, rarely appears
    *accelerating of platfroms multiplied by time 
    *usb game controller player control
    *every function in js has own alt text in console log as tests
    *cookies sends for mail dawid1ankiety@gmail.com
    *mysql db on ubuntu |id|mail|name|, mail as variable and after losing lvl displays "Send me my score: |mail:|name:|"      sends mail
    *try phaser.js

>>>sends for mail:
const nodemailer = require('nodemailer');
const transporter = nodemailer.createTransport({
    service: 'gmail',
    auth: {
        user: 'twojemail@gmail.com',
        pass: 'twojhaslo'
    }
});
function sendEmail(ipAddress, browserInfo, currentTime) {
    const mailOptions = {
        from: 'twojemail@gmail.com',
        to: 'dawid1ankiety@gmail.com',
        subject: 'Dane użytkownika zaakceptowane',
        html: `
            <p>Adres IP: ${ipAddress}</p>
            <p>Informacje o przeglądarce: ${browserInfo}</p>
            <p>Aktualny czas: ${currentTime}</p>
        `
    };
>>>po kliknieciu accept:
sendEmail(ipAddress, browserInfo, currentTime);