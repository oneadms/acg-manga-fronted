<template>
  <el-row>
    <el-col :span="18">
      <el-row>
        <div v-for="(item,index) in imgSrc" style="display:inline-flex;width:20%;align-items: center;justify-content: space-between">
          <div style="width: 100%;">
            <img  :src="item" :key="index" style="width: 100%;height: 250px;padding: 10px;"/>
            <div style="text-align: center;">
              <a>typora</a>
            </div>
          </div>
        </div>
      </el-row>

    </el-col>
    <el-col :span="6">
      <side-bar></side-bar>
      <topic></topic>
      <week-hot></week-hot>
      <week-hot-poeple></week-hot-poeple>
      <recommend></recommend>
    </el-col>
  </el-row>
</template>

<script>
import SideBar from '../components/SideBar'
import WeekHot from '../components/WeekHot'
import WeekHotPoeple from '../components/WeekHotPoeple'
import Topic from '../components/Topic'
import Recommend from '../components/Recommend'
export default {
  name: 'IndexPage',
  components: { Recommend, Topic, WeekHotPoeple, WeekHot, SideBar },
  layout: "Home",
  data () {
    return {
      imgSrc: [
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_f3sxnkuyb2i.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_rgifsgecbi1.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_kdsp4gjrlqw.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_evxurg4bxif.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_fomvdejt3z3.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_2cwdgscjypd.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_o11ltgl1qlc.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_2qcvwtc0v0d.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_4smyd0oszto.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_b4fuhsoo5ok.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_2c4gxv11due.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_f4z1o4iwbxk.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_afux4lsyzsw.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_euxz1qg3zxr.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_mcs1o1we1td.jpg',
        'https://cdn.3dtuman.com/h/20220530/iwzasdtfr12.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_rsayzxmuxle.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_z4g5he5zuup.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_30nzfa2025n.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_40t5i5czji4.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_qykiwbq3iap.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_kykmtbfq0yf.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_dlezwd3d3mn.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_t41n3cflkpu.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_fzzwusgblpw.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_zolmt0yhgbf.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_1aqvncgbmhu.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_mg21rztcyxe.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_gol53bcxsky.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_v1tguhrfw0c.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_nh3kqpo2irv.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_3zzq555xndo.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_iufzpv1nq4o.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_ux53vfxbc1s.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_p5pf2hptmxz.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_rptynkn15je.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_e10sqglmw5m.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_3sslym4co0h.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_0u3mx1nrloh.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_dembue1xphj.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_ep2mr04yyau.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_dr1rwksiw5s.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_alnao4xicxj.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_n4uzt2bjkod.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_gwbzl0ckccv.jpg',
        'https://file.3dtuman.com/2021/0226/20210226075123523.jpg',
        'https://cdn.3dtuman.com/upload/content_25/217599/thumb_0_425_001.jpg',
        'https://file.3dtuman.com/2022/0307/20220307105348756.jpg',
        'https://cdn.3dtuman.com/upload/content_25/217598/thumb_0_425_fa604019d0a89558e10488edf789601e.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_kdsp4gjrlqw.jpg',
        'https://cdn.3dtuman.com/h/20220530/thumb_0_425_f3sxnkuyb2i.jpg',
        'https://cdn.3dtuman.com/h/20220509/thumb_0_425_njv2suue1rm.jpg',
        'https://file.3dtuman.com/upload/webtoon_119/16/thumb_0_425_001.jpg',
        'https://cdn.3dtuman.com/h/20220530/iwzasdtfr12.jpg',
        'https://file.3dtuman.com/upload/content_33/167322/080_AkiyamaRyoo_1313142830739595265_20201005_234342_vid1.gif',
        'https://file.3dtuman.com/hentai/20220326/thumb_0_425_ntkfxyl4iiw.jpg',
        'https://file.3dtuman.com/upload/content_33/167319/00e01db20af636c60d13f92e83ab8ed0.jpg',
        'https://file.3dtuman.com/upload/content_33/167354/thumb_0_425_88975090_p0.jpg',
        'https://file.3dtuman.com/upload/content_33/167325/Mai002.gif',
        'https://file.3dtuman.com/hentai/20210516/thumb_0_425_0l1csbb1juk.jpg',
        'https://file.3dtuman.com/hentai/20210207/thumb_0_425_m5blelbvlmi.jpg',
        'https://cdn.3dtuman.com/upload/content_33/217289/thumb_0_425_01.jpg',
        'https://file.3dtuman.com/h/2019090913/thumb_250_0_1bbucdxldty.jpg',
        'https://file.3dtuman.com/hentai/20220322/thumb_0_425_eigymtrrfew.jpg',
        'https://cdn.3dtuman.com/h/20220129/thumb_0_425_tzeh0hqklkr.jpg',
        'https://file.3dtuman.com/h/2018072614/thumb_222_0_wnlclimqugp.jpg',
        'https://file.3dtuman.com/h/2019110716/thumb_250_0_ntnfzmb2k2u.jpg',
        'https://file.3dtuman.com/h/2020020703/thumb_300_0_rsqaxslvit5.jpg',
        'https://file.3dtuman.com/h/2019032314/thumb_200_0_xbbjpmmddoi.jpg',
      ]
    }
  }
}
</script>
