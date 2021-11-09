<template>
  <section class="Form">
    <form class="Form_Inner">
      <div class="Form_TopicArea">
        <label class="Form_TopicLabel">お問い合わせ内容</label>

        <div class="Form_TopicCheckbox">
          <div class="Form_documentArea">
            <input class="Form_DocumentCheckbox" type="checkbox" id="document" name="document">
            <label class="Form_DocumentLabel" for="document">資料請求</label>
          </div><!-- /.Form_documentArea -->

          <div class="Form_counsellingArea">
            <input class="Form_CounsellingCheckbox" type="checkbox" id="counselling" name="counselling">
            <label class="Form_CounsellingLabel" for="counselling">お電話でのご相談を希望</label>
          </div><!-- /.Form_counsellingArea -->

          <div class="Form_applicationArea">
            <input class="Form_ApplicationCheckbox" type="checkbox" id="application" name="application">
            <label class="Form_ApplicationLabel" for="application">申し込み</label>
          </div><!-- /.Form_applicationArea -->
        </div>
      </div><!-- /.Form_TopicArea -->

      <div class="Form_NameArea">
        <label class="Form_NameLabel" for="name">担当者名</label>
        <input class="Form_NameInput" type="text" id="name">
      </div><!-- /.Form_NameArea -->

      <div class="Form_TelArea">
        <label class="Form_TelLabel" for="tel">電話番号</label>
        <input class="Form_TelInput" type="text" id="tel">
      </div><!-- /.Form_TelArea -->

      <div class="Form_EmailArea">
        <label class="Form_EmailLabel" for="email">メールアドレス</label>
        <input class="Form_EmailInput" type="text" id="email">
      </div><!-- /.Form_mailArea -->

      <div class="Form_OtherArea">
        <label class="Form_OtherLabel" for="other">その他</label>
        <textarea class="Form_OtherInput" name="other" id="other"></textarea>
      </div><!-- /.Form_OtherArea -->
      
    </form><!-- /.Form_Inner -->
  </section><!-- /.Form -->
</template>

<script>
export default {
  name: 'Form'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .Form_Inner {
    max-width: 700px;
    margin-right: auto;
    margin-left: auto;
  }
  .Form_Inner > *:last-child {
    margin-bottom: 0;
  }
  .Form_DocumentLabel, .Form_CounsellingLabel, .Form_ApplicationLabel {
    margin-right: 20px;
    line-height: 1.1875;
    letter-spacing: 0.05em;
  }
  .Form_DocumentCheckbox, .Form_CounsellingCheckbox, .Form_ApplicationCheckbox {
    margin-right: 10px;
  }
  .Form_TopicArea, .Form_NameArea, .Form_TelArea, .Form_EmailArea, .Form_OtherArea {
    display: flex;
    flex-direction: column;
    text-align: left;
    margin-bottom: 25px;
  }
  .Form_NameInput, .Form_TelInput, .Form_EmailInput, .Form_OtherInput {
    width: 100%;
    border: 1px solid #141414;
  }
  .Form_NameInput, .Form_TelInput, .Form_EmailInput {
    height: 1.875rem;
  }
  .Form_OtherInput {
    height: 10.6875rem;
  }
  .Form_TopicCheckbox {
    display: flex;
  }
  .Form_TopicLabel, .Form_NameLabel, .Form_TelLabel, .Form_EmailLabel, .Form_OtherLabel {
    font-weight: bold;
    line-height: 1.875;
    letter-spacing: 0.05em;
  }
  @media screen and (max-width: 414px) {
    .Form_Inner {
      max-width: 90%;
    }
    .Form_TopicCheckbox {
      flex-direction: column;
    }
  }
</style>
