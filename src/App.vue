<template>
  <v-app light>
    <v-toolbar class="white">
      <v-toolbar-title>Gem Designs</v-toolbar-title><v-subheader>since 1986</v-subheader>
    </v-toolbar>
    <v-parallax src="static/images/background1.png" height="100%">
      <v-layout column align-center justify-center>
        <v-carousel hide-delimiters hide-controls style="height:188px; width: 333px; margin-top: 1%; margin-bottom: 1%">
            <v-carousel-item v-for="(item,i) in items" :src="item.src" :key="i"></v-carousel-item>
        </v-carousel>
        <div class="subheading mb-3 text-xs-center">歡迎代購來本店購物，保證隨到立即服務，勿須等候；亦可電話或微信定購，本店提供送貨到府服務。全程可用普通話或英語服務。</div>
        <v-layout row align-center>
          <v-flex xs12 sm12>
            <coverflow :coverList="coverList" :coverWidth="260" :index="2" style="min-height: 300px;"></coverflow>
          </v-flex>
        </v-layout>
        <v-layout row wrap align-center>
              <v-flex xs12 sm3 offset-sm2>
                <v-card class="elevation-0 transparent">
                  <v-card-title primary-title>
                    <div class="headline">Company info</div>
                    <div style="margin-top: 10px;">我們代理：Pandora 和 Thomas Sabo 的 Pearl,
                    10K/14K/18K gold earrings, necklace,
                    Diamondd jewelry, Color Gem Stone Jewelry.</div>
                    <div>We do jewelry repair, remodeling, pearl restring.</div>
                    <div>歡迎代購來本店購物，保證隨到立即服務，勿須等候；亦可電話或微信定購，本店提供送貨到府服務。全程可用普通話或英語服務。</div>
                  </v-card-title>
                </v-card>
              </v-flex>
              <v-flex xs12 sm3 offset-sm1>
                <v-card class="elevation-0 transparent">
                  <v-container fluid grid-list-lg>
                    <v-layout row>
                      <v-flex>
                        <div class="headline">Contact us</div>
                        <div style="margin-top: 10px;">詳情請洽 Sabrina (李太太)</div>
                        <v-list two-line class="transparent">
                          <v-list-tile>
                            <v-list-tile-action>
                              <v-icon class="blue--text">phone</v-icon>
                            </v-list-tile-action>
                            <v-list-tile-content>
                              <v-list-tile-title>(416)591-7143</v-list-tile-title>
                              <v-list-tile-sub-title>Mobile</v-list-tile-sub-title>
                            </v-list-tile-content>
                            </v-list-tile>
                            <v-list-tile>
                              <v-list-tile-action></v-list-tile-action>
                              <v-list-tile-content>
                                <v-list-tile-title>(416)828-9387</v-list-tile-title>
                                <v-list-tile-sub-title>Work</v-list-tile-sub-title>
                              </v-list-tile-content>
                            </v-list-tile>
                            <v-list-tile>
                              <v-list-tile-action>
                                <v-icon class="blue--text">location_on</v-icon>
                              </v-list-tile-action>
                              <v-list-tile-content>
                                <v-list-tile-title>40 Dundas Street</v-list-tile-title>
                                <v-list-tile-sub-title>Toronto, ON M5G 2C2</v-list-tile-sub-title>
                              </v-list-tile-content>
                            </v-list-tile>
                          </v-list>
                          <v-card-media src="static/images/qrcode1.jpg" height="150px" contain></v-card-media>
                        </v-flex>
                      </v-layout>
                    </v-container>
                </v-card>
              </v-flex>
            </v-layout>
        </v-layout>
      </v-parallax>
  </v-app>
</template>

<script>
import Coverflow from './components/Coverflow'
import 'vuetify/dist/vuetify.min.css'
var flyer = require('./json/flyer.json')
var product = require('./json/product.json')

export default {
  name: 'App',
  data () {
    return {
      items: flyer,
      coverList: product
    }
  },
  components: {
    Coverflow
  }
}
</script>
