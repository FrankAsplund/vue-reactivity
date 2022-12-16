<template>
  <main>
    <div class="frame-1">
      <div class="frame-4">
        <div class="skapa-anv-ndarkonto">Skapa användarkonto</div>

        <div
          class="h-r-kan-du-skapa-ett-nytt-anv-ndarkonto-i-ad--v-nligen-fyll-i-uppgifterna-nedan-"
        >
          Här kan du skapa ett nytt användarkonto i AD. Vänligen fyll i
          uppgifterna nedan.
        </div>

        <div class="frame-5">
          <div class="ny-anv-ndare">Ny användare</div>

          <div class="f-rnamn--">
            <span>
              <span class="f-rnamn---span">Förnamn </span>
            </span>
          </div>

          <input />

          <div class="efternamn--">
            <span>
              <span class="efternamn---span">Efternamn </span>
            </span>
          </div>

          <input />

          <div class="prelimin-rt-anv-ndarnamn">Preliminärt användarnamn</div>

          <div class="rectangle-3"></div>

          <div class="prelimin-r-e-postadress">Preliminär e-postadress</div>

          <div class="rectangle-4"></div>

          <div class="titel">Titel</div>

          <input />

          <div class="telefonnummer--">
            <span
              ><span class="telefonnummer---span">Telefonnummer </span
              ><span class="telefonnummer---span2">*</span></span
            >
          </div>

          <input />

          <div class="bolag--">
            <span
              ><span class="bolag---span">Bolag </span
              ><span class="bolag---span2">*</span></span
            >
          </div>

          <input />

          <div class="avdelning--">
            <span
              ><span class="avdelning---span">Avdelning </span
              ><span class="avdelning---span2">*</span></span
            >
          </div>

          <input />

          <div class="chef">Chef</div>

          <input />

          <div class="utg-ngsdatum">Utgångsdatum</div>

          <input />

          <div class="system">System</div>

          <input />

          <div class="mappar">Mappar</div>

          <input />

          <div class="rectangle-13"></div>

          <div class="skicka">Skicka<br /></div>

          <div class="rectangle-14"></div>

          <div class="tillbaka">Tillbaka</div>

          <div class="beh-righet">Behörighet</div>
        </div>
      </div>

      <div class="frame-2">
        <div class="fyll-i-formul-r">Fyll I formulär</div>

        <div class="frame-3">
          <div class="line-3"></div>

          <div class="line-2"></div>

          <div class="line-1"></div>
        </div>

        <div class="image-1"></div>
      </div>
    </div>
  </main>
</template>

<style>
main {
  display: flex;
  justify-content: center;
}

.frame-1,
.frame-1 * {
  box-sizing: border-box;
}
.frame-1 {
  background: #ffffff;
  width: 1051px;
  height: 1553px;
  position: relative;
  overflow: hidden;
}
.frame-4 {
  background: #354b58;
  width: 1051px;
  height: 1497px;
  position: absolute;
  left: 0px;
  top: 56px;
  overflow: hidden;
}
.skapa-anv-ndarkonto {
  color: #ffffff;
  text-align: left;
  font: 400 40px "Inter", sans-serif;
  position: absolute;
  left: 317px;
  top: 21px;
  width: 475px;
  height: 60px;
}
.h-r-kan-du-skapa-ett-nytt-anv-ndarkonto-i-ad--v-nligen-fyll-i-uppgifterna-nedan- {
  color: #ffffff;
  text-align: left;
  font: 400 20px "Inter", sans-serif;
  position: absolute;
  left: 156px;
  top: 91px;
  width: 797px;
  height: 55px;
}
.frame-5 {
  background: #ffffff;
  border-radius: 5px;
  width: 890px;
  height: 1266px;
  position: absolute;
  left: 84px;
  top: 146px;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  overflow: hidden;
}
.ny-anv-ndare {
  color: #000000;
  text-align: left;
  font: 400 20px "Inter", sans-serif;
  position: absolute;
  left: 13px;
  top: 11px;
  width: 168px;
  height: 47px;
}
.f-rnamn-- {
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 14px;
  top: 67px;
  width: 111px;
  height: 36px;
}
.f-rnamn---span {
  color: #000000;
  font: 300 16px "Inter", sans-serif;
}
/* input {
  color: linear-gradient(to left, #ff0000, #ff0000),
    linear-gradient(to left, #000000, #000000);
  font: 300 16px "Inter", sans-serif;
} */

input {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  /* Fix so the positioning is the same, but relative and not absolute */
  position: absolute;
  left: 13px;
  top: 91px;
}

.rectangle-1 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 13px;
  top: 91px;
}
.efternamn-- {
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 14px;
  top: 157px;
  width: 111px;
  height: 36px;
}
.efternamn---span {
  color: #000000;
  font: 300 16px "Inter", sans-serif;
}
.efternamn---span2 {
  color: linear-gradient(to left, #ff0000, #ff0000),
    linear-gradient(to left, #000000, #000000);
  font: 300 16px "Inter", sans-serif;
}
.rectangle-2 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 13px;
  top: 181px;
}
.prelimin-rt-anv-ndarnamn {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 15px;
  top: 247px;
  width: 251px;
  height: 36px;
}
.rectangle-3 {
  background: linear-gradient(to left, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    linear-gradient(to left, #ffffff, #ffffff);
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 14px;
  top: 271px;
}
.prelimin-r-e-postadress {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 16px;
  top: 337px;
  width: 275px;
  height: 36px;
}
.rectangle-4 {
  background: linear-gradient(to left, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    linear-gradient(to left, #ffffff, #ffffff);
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 15px;
  top: 361px;
}
.titel {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 17px;
  top: 427px;
  width: 111px;
  height: 36px;
}
.rectangle-5 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 16px;
  top: 451px;
}
.telefonnummer-- {
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 14px;
  top: 517px;
  width: 153px;
  height: 36px;
}
.telefonnummer---span {
  color: #000000;
  font: 300 16px "Inter", sans-serif;
}
.telefonnummer---span2 {
  color: linear-gradient(to left, #ff0000, #ff0000),
    linear-gradient(to left, #000000, #000000);
  font: 300 16px "Inter", sans-serif;
}
.rectangle-6 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 13px;
  top: 541px;
}
.bolag-- {
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 14px;
  top: 607px;
  width: 111px;
  height: 36px;
}
.bolag---span {
  color: #000000;
  font: 300 16px "Inter", sans-serif;
}
.bolag---span2 {
  color: linear-gradient(to left, #ff0000, #ff0000),
    linear-gradient(to left, #000000, #000000);
  font: 300 16px "Inter", sans-serif;
}
.rectangle-7 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 13px;
  top: 631px;
}
.avdelning-- {
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 14px;
  top: 697px;
  width: 111px;
  height: 36px;
}
.avdelning---span {
  color: #000000;
  font: 300 16px "Inter", sans-serif;
}
.avdelning---span2 {
  color: linear-gradient(to left, #ff0000, #ff0000),
    linear-gradient(to left, #000000, #000000);
  font: 300 16px "Inter", sans-serif;
}
.rectangle-8 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 13px;
  top: 721px;
}
.chef {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 15px;
  top: 787px;
  width: 111px;
  height: 36px;
}
.rectangle-9 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 14px;
  top: 811px;
}
.utg-ngsdatum {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 16px;
  top: 877px;
  width: 111px;
  height: 36px;
}
.rectangle-10 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 15px;
  top: 901px;
}
.system {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 16px;
  top: 1004px;
  width: 111px;
  height: 36px;
}
.rectangle-11 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 15px;
  top: 1028px;
}
.mappar {
  color: #000000;
  text-align: left;
  font: 300 16px "Inter", sans-serif;
  position: absolute;
  left: 13px;
  top: 1094px;
  width: 111px;
  height: 36px;
}
.rectangle-12 {
  background: #ffffff;
  border: solid #000000;
  border-width: 1px;
  width: 863px;
  height: 43px;
  position: absolute;
  left: 12px;
  top: 1118px;
}
.rectangle-13 {
  background: #4a90e2;
  border-radius: 6px;
  width: 89px;
  height: 36px;
  position: absolute;
  left: 16px;
  top: 1193px;
}
.skicka {
  color: #ffffff;
  text-align: left;
  font: 400 16px "Inter", sans-serif;
  position: absolute;
  left: 35px;
  top: 1201px;
  width: 79px;
  height: 27px;
}
.rectangle-14 {
  background: #0275d8;
  border-radius: 6px;
  width: 89px;
  height: 36px;
  position: absolute;
  left: 124px;
  top: 1193px;
}
.tillbaka {
  color: #ffffff;
  text-align: left;
  font: 400 16px "Inter", sans-serif;
  position: absolute;
  left: 137px;
  top: 1202px;
  width: 79px;
  height: 27px;
}
.beh-righet {
  color: #000000;
  text-align: left;
  font: 400 20px "Inter", sans-serif;
  position: absolute;
  left: 12px;
  top: 964px;
  width: 168px;
  height: 47px;
}
.frame-2 {
  width: 1051px;
  height: 52px;
  position: absolute;
  left: 0px;
  top: 0px;
  overflow: hidden;
}
.fyll-i-formul-r {
  color: #000000;
  text-align: left;
  font: 400 20px "Inter", sans-serif;
  position: absolute;
  left: 62px;
  top: 18px;
  width: 157px;
  height: 34px;
}
.frame-3 {
  width: 45px;
  height: 42px;
  position: absolute;
  left: 14px;
  top: 14px;
  overflow: hidden;
}
.line-3 {
  border: solid #000000;
  border-width: 2px 0 0 0;
  width: 16px;
  height: 0px;
  position: absolute;
  left: 9px;
  top: 23px;
}
.line-2 {
  border: solid #000000;
  border-width: 2px 0 0 0;
  width: 16px;
  height: 0px;
  position: absolute;
  left: 9px;
  top: 17px;
}
.line-1 {
  border: solid #000000;
  border-width: 2px 0 0 0;
  width: 16px;
  height: 0px;
  position: absolute;
  left: 9px;
  top: 11px;
}
.image-1 {
  width: 92px;
  height: 43px;
  position: absolute;
  left: 946px;
  top: 10px;
}
</style>
