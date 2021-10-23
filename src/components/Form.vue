<template>
  <section class="form">
    <form class="form__inner">
      <div class="form__topic-area">
        <label class="form__topic-label">お問い合わせ内容</label>

        <div class="form__topic-checkbox">
          <input class="form__document-checkbox" type="checkbox" id="document" name="document">
          <label class="form__document-label" for="document">資料請求</label>

          <input class="form__counselling-checkbox" type="checkbox" id="counselling" name="counselling">
          <label class="form__counselling-label" for="counselling">お電話でのご相談を希望</label>

          <input class="form__applicationß-checkbox" type="checkbox" id="application" name="application">
          <label class="form__application-label" for="application">申し込み</label>
        </div>
      </div><!-- /.form__topic-area -->

      <div class="form__name-area">
        <label class="form__name-label" for="name">担当者名</label>
        <input class="form__name-input" type="text" id="name">
      </div><!-- /.form__name-area -->

      <div class="form__tel-area">
        <label class="form__tel-label" for="tel">電話番号</label>
        <input class="form__tel-input" type="text" id="tel">
      </div><!-- /.form__tel-area -->

      <div class="form__email-area">
        <label class="form__email-label" for="email">メールアドレス</label>
        <input class="form__email-input" type="text" id="email">
      </div><!-- /.form__mail-area -->

      <div class="form__other-area">
        <label class="form__other-label" for="other">その他</label>
        <textarea class="form__other-input" name="other" id="other"></textarea>
      </div><!-- /.form__other-area -->
      
    </form><!-- /.form__inner -->
  </section><!-- /.form -->
</template>

<script>
export default {
  name: 'Form'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .form {

  }

  .form__inner {
    max-width: 700px;
    margin-right: auto;
    margin-left: auto;
  }

  .form__inner > *:last-child {
    margin-bottom: 0;
  }

  .form__document-label, .form__counselling-label, .form__document-label {
    margin-right: 20px;
  }

  .form__document-checkbox, .form__counselling-checkbox, .form__applicationß-checkbox {
    margin-right: 10px;
  }

  .form__topic-area, .form__name-area, .form__tel-area, .form__email-area, .form__other-area {
    display: flex;
    flex-direction: column;
    text-align: left;
    margin-bottom: 25px;
  }

  .form__name-input, .form__tel-input, .form__email-input, .form__other-input {
    width: 100%;
    border: 1px solid #141414;
  }

  .form__name-input, .form__tel-input, .form__email-input {
    height: 1.875rem;
  }

  .form__other-input {
    height: 10.6875rem;
  }

  .form__topic-label, .form__name-label, .form__tel-label, .form__email-label, .form__other-label {
    font-weight: bold;
  }

  @media screen and (max-width: 414px) {

    .form {

    }

    .form__inner {
      
    }

  }
  
</style>
