<template lang="pug">
  #app
    main
      .step
        span.step__item.step__item--activity 1
        span.step__item 2
        span.step__item 3
      .main-container
        .order
          .order-container
            .order__title
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
          .button 返回商店
        .content
          h1.content__title STEP1. 選擇付款方式
          .radio-container
            input.radio__control(type="radio" name="shopAPI" id="card")
            label.radio__item(for="card")
              img(src="./assets/images/credit-card.svg")
              .radio__title 信用卡/金融卡
            input.radio__control(type="radio" name="shopAPI" id="unionpay")
            label.radio__item(for="unionpay")
              img(src="./assets/images/unionpay.svg")
              .radio__title 銀聯卡
            input.radio__control(type="radio" name="shopAPI" id="shop")
            label.radio__item(for="shop")
              img(src="./assets/images/shop.svg")
              .radio__title 超商付款
            input.radio__control(type="radio" name="shopAPI" id="webAtm")
            label.radio__item(for="webAtm")
              img(src="./assets/images/web-atm.svg")
              .radio__title Web ATM
            input.radio__control(type="radio" name="shopAPI" id="atm")
            label.radio__item(for="atm")
              img(src="./assets/images/atm.svg")
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
.step
  padding: 40px;
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
    &--activity
      background: #8DEFCB;
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
  &__title
    font-size: 20px;
    color: #000000;
    letter-spacing: 2.09px;
    margin-bottom: 90px;
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
  &__title
    margin-top: 10px;
  &__control
    display: none;
    &:checked + .radio__item
      background: #36B996;
</style>
