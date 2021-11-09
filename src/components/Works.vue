<template>
  <section class="Works" id="works">
    <div class="Works_Inner">
      <h2 class="Works_Title">Works</h2><!-- /.Works_Title -->
      <div class="Works_Cards">
        <Card 
          class="Works_Card"
          text="新規サイトを公開しました。今回のサイトは白と黒を基調にしたミニマルなデザインになっています。" 
          fileName="card-img01@2x.jpg"
          alt="オフィスの風景">
        </Card>
        <Card 
          class="Works_Card"
          text="新規サイトを公開しました。今回のサイトは白と黒を基調にした。"
          fileName="card-img02@2x.jpg"
          alt="会議室の風景">
        </Card>
        <Card 
          class="Works_Card"
          text="新規サイトを公開しました。今回のサイトは白と黒を基調にしたミニマルなデザインになっています。"
          fileName="card-img03@2x.jpg"
          alt="休憩室の風景">
        </Card>
      </div><!-- /.Works_Cards -->
      <div class="Works_Btn">
        <Button text="View more"></Button>
      </div><!-- /.Works_Btn -->
      <div class="Works_BackgroundText">Our Works</div><!-- /.Works_BackgroundText -->
    </div><!-- /.Works_Inner -->
  </section><!-- /.Works -->
</template>

<script>
import Card from './Card.vue' 
import Button from './Button.vue' 

export default {
  name: 'Works',
  components: {
    Card,
    Button
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .Works {
    background-image: url("../assets/img/works-bgi@2x.jpg");
    background-size: cover;
  }
  .Works_Inner {
    padding: 104px 120px 70px;
  }
  .Works_Title {
    color: #fff;
    font-size: 3.75rem;
    font-style: italic;
    font-weight: bold;
    letter-spacing: .1em;
    line-height: .8;
    margin-bottom: 80px;
    position: relative;
    text-align: right;
    transform: translateX(-230px);
  }
  .Works_Title::after {
    border: 3px solid #fff;
    content: "";
    display: inline-block;
    margin-left: 30px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 200px;
  }
  .Works_Cards {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    margin-bottom: 80px;
  }
  .Works_Btn {
    margin-bottom: 70px;
  }
  .Works_BackgroundText {
    color: rgba(255,255,255,.05);
    font-size: 5.625rem;
    font-weight: bold;
    letter-spacing: .05em;
    line-height: 1.66667;
    text-align: left;
  }
  @media screen and (max-width: $tb) {
    .Works_Cards {
      flex-direction: column;
    }
    .Works_Card {
      margin-left: auto;
      margin-right: auto;
      width: 100%;
    }
  }
  @media screen and (max-width: $sp) {
    .Works_Inner {
      padding: 100px 15px 40px;
    }
    .Works_Title {
      font-size: 1.875rem;
      transform: translateX(-120px);
    }
    .Works_Title::after {
      margin-left: 30px;
      width: 90px;
    }
    .Works_BackgroundText {
      font-size: 2.5rem;
    }
  }

</style>
