<template>
  <div>
    <div class="heading-style border color-main position-sticky">
      <span class="color-primary">Q</span>uote
    </div>
    <div class="quote-profile">
      <div class="text">
        I hereby declare that the above written particulars are true to the best
        of my knowledge and belief.
      </div>
      <div class="flex-column flex-class">
        <img
          class="quote-photo"
          src="~/assets/img/IMG_20210709_114540_006.jpeg"
          alt=""
        />

        <div class="color-main quote-name">Varnika Jain</div>
        <div>Software Developer and QA</div>
      </div>
    </div>
  </div>
</template>

<style>
.quote-profile {
  padding: 2rem;
}
.text {
  text-align: center;
  position: relative;
  padding: 0 30px;
  font-weight: 300;
  font-style: italic;
  opacity: 0.65;
  margin-bottom: 2rem;
}
.text::before {
  content: "";
  position: absolute;
  left: 3px;
  top: 3px;
  width: 14px;
  height: 14px;
  background: url(~/assets/img/quote-left.svg) no-repeat;
  background-size: contain;
  opacity: 0.75;
}
.text::after {
  content: "";
  position: absolute;
  right: 3px;
  bottom: 3px;
  width: 14px;
  height: 14px;
  background: url(~/assets/img/quote-right.svg) no-repeat;
  background-size: contain;
  opacity: 0.75;
}
.quote-photo {
  width: 70px;
  height: 70px;
  border-radius: 50%;
}
.quote-name {
  font-size: 1rem;
  font-weight: 600;
  margin: 10px 0px 3px 0px;
}
</style>