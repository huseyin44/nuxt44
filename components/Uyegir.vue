<template>
  <div>
    <v-container>
      <v-row><div class="uyegirisi">Üye Girişi</div></v-row>
      <v-row class="buton1"></v-row>
      <v-row><div class="birinciemail">Email Adresiniz</div></v-row>
      <v-row class="buton1"></v-row>
      <v-row>
        <input type="email" autocapitalize="off" autocorrect="off" spellcheck="false" v-model="user.email"
        class="inputemail"/>
      </v-row>
      <v-row class="buton1"></v-row>
      <v-row><div class="birinciemail">Şifre</div></v-row>
      <v-row class="buton1"></v-row>
      <v-row>
        <input type="password" autocapitalize="off" autocorrect="off" spellcheck="false" v-model="user.sifre"
        class="inputemail" />
      </v-row>
      <v-row class="buton1"></v-row>
      <v-row>
      <div :class="{ red40 : gecersiz40 }" @mouseover="kirmizi40" @mouseleave="gecersiz40=false" class="sifre11">Şifrenizi mi unuttunuz ?</div>
      </v-row>
      <v-row class="buton1"></v-row>
      <v-row class="buton1"></v-row>
      <v-row>
       <div :class="{ red41 : gecersiz41 }" @mouseover="kirmizi41" @mouseleave="gecersiz41=false" class="uyegirisibut">ÜYE GİRİŞİ</div>
      </v-row>
      <v-row class="buton1"></v-row>
      <v-row class="buton1"></v-row>
      <v-row>
        <div class="facebook">
         <a href="https://graph.facebook.com/oauth/authorize?client_id=328336257500368&amp;redirect_uri=https%3A%2F%2Fwww.saatvesaat.com.tr%2Fsocialconnect%2Ffacebook%2Fconnect%2F&amp;state=968c0ff130b664635e9d4f2c0710cc65&amp;scope=email%2Cuser_birthday" rel="facebook-connect" class="button mnm-button connect-facebook inline">
           <span><i class="ion-social-facebook"></i> Facebook ile Giriş Yap</span>
        </a>
        </div>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    gecersiz40: false,
    gecersiz41: false,
    user: {
       email: '12345',
       sifre: '12345',
    },
  }),
   methods:{
   kirmizi40() {
    this.gecersiz40 = true;},
   kirmizi41() {
   this.gecersiz41 = true; },}
}
</script>

<style>
.uyegirisi{
  font-size: 24px;
  font-weight: 500;
  color: #353535;
}
.birinciemail{
  font-size: 12px;
  font-family: "Roboto", Arial, sans-serif;
  font-weight: 500;
}
.inputemail{
    background-color: transparent;
    border-style:solid;
}
.buton1{
  height: 4px;
}
.sifre11{
  color: red;
}
.red40 {
  color: red;text-decoration: underline;
}
.uyegirisibut{
  background: #9c0c0c;
  font-size: 14px;
  height: 40px;
  width: 130px;
  color: white;
  text-align:center ;
  padding: 7px 15px;
}
.red41 {
  color: black;
  background: white;
  border-style:solid;
  border-color:black;
}
.facebook{
  background:blue;
  display: inline-block;
  padding: 25px 25px;
  border: 2px solid transparent;
  color: #FFFFFF;
  font-size: 12px;
  font-weight: normal;
  font-family: "Roboto", Arial, sans-serif;
  line-height: 19px;
  text-align: center;
  text-transform: uppercase;
  vertical-align: middle;
  white-space: nowrap;
}
</style>