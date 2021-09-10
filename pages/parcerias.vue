<template>
  <div class="p-2">
    <header class="d-flex justify-content-center">
      <Header
        :text="'Clique em uma das nossas lojas parceiras'"
        :to="'/'"
       />
    </header>
    <div class="person">
      <div class="container">
        <div class="container-inner">
          <img class="img img1" src="~/assets/images/logo-sul.png" />
        </div>
      </div>
      <div class="divider"></div>
      <div class="name">Sul Concept</div>
      <div class="title">Surf Shop / Skate Shop</div>
    </div>
    <div class="person">
      <div class="container">
        <div class="container-inner">
          <img class="img img2" />
        </div>
      </div>
      <div class="divider"></div>
      <div class="name">Jak</div>
      <div class="title">Vestuário Feminino</div>
    </div>
  </div>
</template>
