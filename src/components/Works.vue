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
<style scoped>
  .Works {
    background-image: url("../assets/img/works-bgi@2x.jpg");
    background-size: cover;
  }
  .Works_Inner {
    padding: 104px 120px 70px;
  }
  .Works_Title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    color: #fff;
    text-align: right;
    margin-bottom: 80px;
    transform: translateX(-230px);
    line-height: 0.8;
    letter-spacing: 0.1em;
  }
  .Works_Title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #fff;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }
  .Works_Cards {
    margin-bottom: 80px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
  .Works_Btn {
    margin-bottom: 70px;
  }
  .Works_BackgroundText {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
    line-height: 1.66667;
    letter-spacing: 0.05em;
  }
  @media screen and (max-width: 1080px) {
    .Works_Cards {
      flex-direction: column;
    }
    .Works_Card {
      width: 100%;
      margin-right: auto;
      margin-left: auto;
    }
  }
  @media screen and (max-width: 414px) {
    .Works_Inner {
      padding: 100px 15px 40px;
    }
    .Works_Title {
      font-size: 1.875rem;
      transform: translateX(-120px);
    }
    .Works_Title::after {
      width: 90px;
      margin-left: 30px;
    }
    .Works_BackgroundText {
      font-size: 2.5rem;
    }
  }
</style>
