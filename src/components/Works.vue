<template>
  <section class="works" id="works">
    <div class="works__inner">
      <h2 class="works__title">Works</h2><!-- /.works__title -->
      <div class="works__cards">
        <Card 
          text="新規サイトを公開しました。今回のサイトは白と黒を基調にしたミニマルなデザインになっています。" 
          fileName="card-img01@2x.jpg"
          alt="オフィスの風景">
        </Card>
        <Card 
          text="新規サイトを公開しました。今回のサイトは白と黒を基調にした。"
          fileName="card-img02@2x.jpg"
          alt="会議室の風景">
        </Card>
        <Card 
          text="新規サイトを公開しました。今回のサイトは白と黒を基調にしたミニマルなデザインになっています。"
          fileName="card-img03@2x.jpg"
          alt="休憩室の風景">
        </Card>
      </div><!-- /.works__cards -->
      <div class="works__btn">
        <Button text="View more"></Button>
      </div><!-- /.works__btn -->
      <div class="works__background-text">Our Works</div><!-- /.works__background-text -->
    </div><!-- /.works__inner -->
  </section><!-- /.works -->
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
  .works {
    background-image: url("../assets/works-bgi@2x.jpg");
    background-size: cover;
  }

  .works__inner {
    padding: 104px 120px 70px;
  }

  .works__title {
    position: relative;
    font-size: 3.75rem;
    font-weight: bold;
    font-style: italic;
    color: #fff;
    text-align: right;
    margin-bottom: 80px;
    transform: translateX(-230px);
  }

  .works__title::after {
    content: '';
    display: inline-block;
    width: 200px;
    border: 3px solid #fff;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    margin-left: 30px;
  }

  .works__cards {
    margin-bottom: 80px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }

  .works__btn {
    margin-bottom: 70px;
  }

  .works__background-text {
    font-size: 5.625rem;
    font-weight: bold;
    color: rgba(255,255,255,.05);
    text-align: left;
  }

  @media screen and (max-width: 1080px) {

    .works__cards {
      flex-direction: column;
    }
    
  }

  @media screen and (max-width: 414px) {

    .works__inner {
      padding: 100px 15px 40px;
    }

    .works__title {
      font-size: 1.875rem;
      transform: translateX(-120px);
    }

    .works__title::after {
      width: 90px;
      margin-left: 30px;
    }

    .works__background-text {
      font-size: 2.5rem;
    }
  }

</style>
