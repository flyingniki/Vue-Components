<script>
export default {};
</script>

<template>
  <div class="container">
    <form class="order-form" action="#" method="post">
      <h2 class="order-form__title">Данные покупателя</h2>
      <ul class="order-form__list">
        <li class="order-form__item text-field">
          <label class="text-field__label" for="name"></label>
          <input
            class="text-field__input"
            type="text"
            name="name"
            id="name"
            placeholder="Контактное лицо*"
          />
        </li>
        <li class="order-form__item text-field">
          <label class="text-field__label" for="phone"></label>
          <input
            class="text-field__input"
            type="tel"
            name="phone"
            id="phone"
            placeholder="Телефон*"
          />
        </li>
        <li class="order-form__item text-field">
          <label class="text-field__label" for="description"></label>
          <input
            class="text-field__input"
            type="text"
            name="description"
            id="description"
            placeholder="ИНН"
          />
        </li>
        <li class="order-form__item text-field">
          <label class="text-field__label" for="email"></label>
          <input
            class="text-field__input"
            type="email"
            name="email"
            id="email"
            placeholder="Email"
          />
        </li>
        <!-- drag & drop start -->
        <li class="order-form__item drag-n-drop">
          <div class="drag-n-drop__container" id="fileinput">
            <img
              class="drag-n-drop__img"
              src="../assets/img/clip.svg"
              alt="clip"
            />
            <div class="drag-n-drop__field">
              <label class="drag-n-drop__label" for="dropedfile"
                >Нажмите ссылку</label
              >
              <input
                class="drag-n-drop__input hidden"
                type="file"
                name="dropedfile"
                id="dropedfile"
                multiple
              />
              <span class="drag-n-drop__span"> чтобы прикрепить реквизиты</span>
            </div>
          </div>
        </li>
        <!-- drag & drop end -->
        <li class="order-form__item comment-area">
          <textarea
            class="comment-area__field"
            name="comment"
            id="comment"
            cols="30"
            rows="10"
            placeholder="Комментарий к заказу"
          ></textarea>
        </li>
      </ul>
      <!-- <div class="order-form__send">
        <button class="order-form__button" type="submit">
          Отправить заявку
        </button>
      </div> -->
    </form>
  </div>
</template>

<style lang="sass" scoped>
*
  font-size: 14px
  line-height: 145%
  font-weight: 500
.hidden
  display: none
.order-form
  box-sizing: border-box
  width: 1032px
  margin: 0 auto
  padding: 30px 32px 53px
  border: 1px solid #d5d5d5
  border-radius: 15px
.order-form__title
  margin: 0
  margin-bottom: 19px
  font-size: 25px
.order-form__list
  list-style: none
  margin: 0
  padding: 0
  display: grid
  grid-template-columns: repeat(2, 1fr)
  grid-gap: 16px
.order-form__item
  width: 476px
.order-form__item:nth-child(5)
  grid-column: 1 / 3
.order-form__item:nth-child(6)
  grid-column: 1 / 3
  width: 100%
.text-field__input
  box-sizing: border-box
  background-color: #edfcff
  width: 100%
  height: 46px
  border: #47bfc7
  border-radius: 10px
  padding: 13px 16px
  color: #47bfc7
.text-field__input::placeholder
  color: #47bfc7
.drag-n-drop
  padding: 14px 16px
.drag-n-drop__container
  display: flex
  align-items: center
  column-gap: 16px
.drag-n-drop__label
  color: #47bfc7
  cursor: pointer
  user-select: none
.comment-area__field
  display: block
  background-color: #edfcff
  border: none
  width: 100%
  height: 111px
  resize: none
  box-sizing: border-box
  padding: 13px 16px
  color: #47bfc7
.comment-area__field::placeholder
  color: #47bfc7
</style>
