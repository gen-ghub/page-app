<template>
  <div>
    <Header />
    <div class="relative">
      <img class="profile-img" src="~/assets/woman2.jpg" />
      <h2 class="profile-title absolute text-white ">YAMADA HANAKO</h2>
    </div>
    <section class="mt-20 mb-32 flex justify-center">
      <div class="flex flex-col items-center space-y-2 text-sm font-thin text-gray-800">
        <h2 class="text-3xl mb-10 font-semibold">プロフィール</h2>
        <p>山田華子</p>
        <p>1983年8月3日生まれ。</p>
        <p>東京都出身。</p>
        <p>慶應義塾幼稚舎、慶應義塾中等部、慶應義塾女子高等学校へ進学</p>
        <p>慶應義塾大学文学部人文社会学科人間科学専攻を卒業</p>
        <p>卒業後（株）LDHに所属、俳優として舞台やドラマに出演し、</p>
        <p>その後（株）BABEL LABELで映画、CMなどを中心に活動。</p>
        <p>2015年ゆうばり国際映画祭では主演作「眠れる美女の限界」(二宮健監督)が審査員特別賞を受賞。</p>
        <p>その後フリーランスとなり、2018年にはヒロインを務めた「スティルライフオブメモリーズ」(矢崎仁司監督)が公開、</p>
        <p>主演を務めた「BIRD SONG」(Hendrik Willemins監督)もベルギーにてワールドプレミア上映される。</p>
        <p>同2018年、芸能界及び表現者とそのサポーターへのメンタルケアを普及するべくOffice GENE（株）を設立。</p>
        <p>自ら代表取締役を務めながら、俳優／カウンセラーとして活動中。</p>
        <p>2019年9月に出産し、一児の母でもある。</p>
      </div>
    </section>
    <section class="mt-20 mb-32 flex justify-center">
      <div class="flex flex-col items-center space-y-2 text-sm font-thin text-gray-800">
        <h2 class="text-3xl mb-10 font-semibold">エンタメ</h2>
        <p>2018 「円盤」萬浪大輔演出@池袋シアターグリーンBOX in BOX</p>
        <p>2016 「ヘナレイデーアゲイン」山内晶演出＠SPACE梟門</p>
        <p>2015 「まっ透明なAsoべんきょ～」粟島瑞丸演出＠中野ザポケット　「青春の門～虚構の劇団vol3」千葉哲也演出＠</p>
        <p>2012 「ウサニ」　永山耕三演出＠ル・テアトル銀座</p>
        <p>2011 「女の平和」　江本純子演出＠俳優座劇場 「Noises Off」　千葉哲也演出＠池袋あうるすぽっと</p>
        <p>2010 「2LDK」　堤幸彦演出＠青山円形劇場</p>
        <p>2009 劇団EXILE JUNCTION3#1「ナイトパレット Night Pallet」
        </p>
      </div>
    </section>
    <section class="mt-20 mb-32 flex justify-center">
      <div class="flex flex-col items-center space-y-2 text-sm font-thin text-gray-800">
        <h2 class="text-3xl mb-10 font-semibold">翻訳</h2>
        <p>2018 「円盤」萬浪大輔演出@池袋シアターグリーンBOX in BOX</p>
        <p>2016 「ヘナレイデーアゲイン」山内晶演出＠SPACE梟門</p>
        <p>2015 「まっ透明なAsoべんきょ～」粟島瑞丸演出＠中野ザポケット　「青春の門～虚構の劇団vol3」千葉哲也演出＠</p>
        <p>2012 「ウサニ」　永山耕三演出＠ル・テアトル銀座</p>
        <p>2011 「女の平和」　江本純子演出＠俳優座劇場 「Noises Off」　千葉哲也演出＠池袋あうるすぽっと</p>
        <p>2010 「2LDK」　堤幸彦演出＠青山円形劇場</p>
        <p>2009 劇団EXILE JUNCTION3#1「ナイトパレット Night Pallet」</p>
      </div>
    </section>
    <div class="mt-20 mb-20 flex justify-center">
      <h2 class="text-xl mb-10 font-thin">etc...</h2>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.profile-img{
  height: 50vh;
  width: 100vw;
  object-fit: cover;
}
.profile-title{
  top: 20vh;
  left: 35vw;
  font-size: 1.5vw;
  font-weight: 300;
}
</style>
