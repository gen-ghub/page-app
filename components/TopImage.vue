<template>
  <section>
    <div class="relative ">
      <img class="h-screen w-screen object-cover" src="~/assets/top.jpg" />
      <div class="absolute inset-0">
        <div class="flex justify-center items-center h-screen w-screen">
          <div class="text-white font-serif ">
            <h2 class="text-5xl font-thin pb-8">Just the way you ane</h2>
            <h4 class="text-2xl font-extralight tracking-widest flex justify-center">OFFICE GENE</h4>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
h2{
  font-family: cursive;
}
  @media screen and (max-width: 425px){
    h2{
      font-size: 40px;
    }
  }
    @media screen and (max-width: 375px){
    h2{
      font-size: 35px;
    }
    h4{
      font-size: 20px;
    }
  }
    @media screen and (max-width: 320px){
    h2{
      font-size: 30px;
    }
    h4{
      font-size: 20px;
    }
  }
</style>
