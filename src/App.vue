<template lang="pug">
  #app
    main
      .step.step--first
        span.step__item 1
        span.step__item 2
        span.step__item 3
      .main-container
        .order
          .order-container
            .order__title 訂單資訊
            p.order__info
              |商品名稱：
              br
              |Iphone XR手機殼 x1
            p.order__info
              |訂單編號：
              br
              |17485739
            p.order__info
              |訂單金額：
              br
              |NT$ 600
          .order__button 返回商店
        .content
          h1.content__title STEP1. 選擇付款方式
          .radio-container
            input.radio__control(type="radio" name="shopAPI" id="card")
            label.radio__item(for="card")
              img.radio__icon(src="./assets/images/credit-card.svg")
              .radio__title 信用卡/金融卡
            input.radio__control(type="radio" name="shopAPI" id="unionpay")
            label.radio__item(for="unionpay")
              img.radio__icon(src="./assets/images/unionpay.svg")
              .radio__title 銀聯卡
            input.radio__control(type="radio" name="shopAPI" id="shop")
            label.radio__item(for="shop")
              img.radio__icon(src="./assets/images/shop.svg")
              .radio__title 超商付款
            input.radio__control(type="radio" name="shopAPI" id="webAtm")
            label.radio__item(for="webAtm")
              img.radio__icon(src="./assets/images/web-atm.svg")
              .radio__title Web ATM
            input.radio__control(type="radio" name="shopAPI" id="atm")
            label.radio__item(for="atm")
              img.radio__icon(src="./assets/images/atm.svg")
              .radio__title ATM 轉帳
          a.shop-button 下一步
</template>

<script>
import './assets/style/normalize.css'
import './assets/style/reset.css'

export default {
  name: 'app',
  components: {
  }
}
</script>
<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
main::after
  content: '';
  position: absolute;
  width: 100%;
  background: url(/img/footer-background.576d29f0.svg) #defff2 center 20px;
  background-size: 60px;
  height: 14vh;
  display: block;
  bottom: 0;
  left: 0;
  z-index: -1;
.step
  padding: 40px;
  &::after
    content: '';
    height: 2px;
    width: 266px;
    background: #eee;
    position: absolute;
    left: 50%;
    margin-left: -133px;
    top: 60px;
    z-index: -1;
  &__item
    width: 40px;
    line-height: 40px;
    display: inline-block;
    color: #fff;
    border-radius: 40px;
    margin: 0 45px;
    background: #D8D8D8;
    font-size: 20px;
    font-family: NotoSansCJKtc-Medium;
  &--first
    ^[-1]__item:nth-child(1)
      background: #8DEFCB;
    &::after
      background: linear-gradient(to right, #8DEFCB 0%, #D8D8D8 33.33%);
.main-container
  max-width: 628px;
  margin: 0 auto;
  position: relative;
  height: calc(100vh - 120px);
.order
  position: absolute;
  width: 234px;
  left: -234px;
  text-align: left;
  line-height: 24px;
  &__title
    font-size: 18px;
    color: #000000;
    letter-spacing: 1.88px;
  &__button
    background: #4B4B4B;
    border-radius: 5px;
    color: #fff;
    display: inline-block;
    padding: 10px 14px;
    margin-top: 24px;
    cursor: pointer;
    font-size: 14px;
    line-height: 19px;
    letter-spacing: 1.46px;
    min-width: 90px;
    text-align: center;
.order-container
  background: #F3F3F3;
  border-radius: 10px 0 0 10px;
  padding: 24px;
.content
  background: #FFFFFF;
  box-shadow: 0 2px 13px 0 rgba(0,0,0,0.08);
  border-radius: 0 10px 0 0;
  padding: 38px 58px;
  height: 100%
  text-align: right;
  &__title
    font-size: 20px;
    color: #000;
    letter-spacing: 2.09px;
    margin-bottom: 90px;
    position: relative;
    z-index: 2;
    display: block;
    padding: 0 10px;
    width: 240px;
    margin: 0 auto 90px;
    &::after
      content: '';
      position: absolute;
      width: 100%;
      display: block;
      bottom: -5px;
      left: 0;
      z-index: -1;
      height: 17px;
      background: #B5FFE4;
.radio-container
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
.radio
  &__item
    margin: 11px 7px;
    width: calc(33.33% - 15px);
    background: #f7f7f7;
    border-radius: 5px;
    padding: 22px 30px;
    font-size: 14px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
    cursor: pointer;
    transition: background .35s ease;
  &__title
    margin-top: 10px;
  &__control
    display: none;
    &:checked
      & + ^[0]
        &__item
          background: #36B996;
          & ^[-4]__icon
            filter: brightness(100);
          & ^[-4]__title
            color: #fff;
.shop-button
  background: #36B996;
  border-radius: 5px;
  color: #fff;
  display: inline-block;
  padding: 10px 14px;
  margin-top: 24px;
  cursor: pointer;
  font-size: 14px;
  line-height: 19px;
  letter-spacing: 1.46px;
  min-width: 90px;
  text-align: center;
</style>
