<template class="template">
  <div class="center">
    <div
      v-for="(item, index) in cocktails"
      :key="index"
      class="idkname"
    >
      <div
        class="main"
      >
        <div class="aside">
          <a>
            <div
              v-for="(part) in item.parts"
              :key="part.part"
              class="cocktail-item-good"
            >
              <img
                class="image"
                :src="'https://ru.inshaker.com' + part.src"
                :title="part.name"
                :width="68"
                :height="68"
              >
              <div class="name"><br><span>{{ part.name }}</span><br></div>
            </div>
          </a>
        </div>
        <section>
          <img
            class="size"
            :src="'https://ru.inshaker.com' + item.src"
          >
          <div class="name-main">
            <span>{{ item.name }}</span>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {
    };
  },
  computed: {
    cocktails() {
      return this.$store.getters.list;
    },
  },
};
</script>

<style>
  .name-main {
    margin-top: 29%;
    margin-left: 0%;
    line-height: 20px;
    width: 120px;
    font: 17px/27px;
    line-height: 29px;
    font-style: italic;
    text-align: center;
    background: white;
  }

  hr {
    border: none;
    border-top: 2px dotted #f00;
    color: #fff;
    background-color: #fff;
    height: 1px;
  }

  .noname {
    border-bottom: 1px dashed #ccc;
    margin-top: 100%;
    width: 1230px;
    height: auto;
    margin-left: -33.5%;

  }

  .center {
    background: white;
    width: 65%;
    height: 100%;
    margin-top: 57.86%;
    margin-left: 22%;
  }

  .name {
    font: 13px/27px "Times New Roman";
    line-height: 29px;
    text-align: center;
    margin-top: -17%;
    margin-left: 91%;
    width: 140px;
    height: 35px;
  }

  span {
    color: black !important;
    font-family: PT Sans, Arial, Tahoma, sans-serif;
  }

  .application--wrap {
    background-image: url("https://ru.inshaker.com/assets/common/body-bg-bf9928ee232a5a485e2d840111ee4bb2b7affb0509ecc283e6c81d4956ca3038.jpg");
    height: auto;
    background-repeat: repeat-y;
  }

  .main {
    line-height: 80px;
    height: auto;
    margin-top: -102%;
    margin-left: -18%;
    background: blue;

  }

  .main1 {
    width: 120px;
    margin-top: 170%;
    height: 300px;
    margin-left: -15%;
    background: white;
  }

  section {
    margin-top: 5%;
    float: left;
    height: auto;
    width: 17%;
    background: white;
  }

  .aside {
    display: flex;
    justify-content: left;
    margin-top: 10%;
    float: right;
    height: 100px;
    width: 95%;

    background: white
  }

  footer {
    clear: both;
    margin-bottom: 0;
  }

  .cocktail-item-good {
    margin-top: 30px;
    position: relative;
    display: inline-block;
    vertical-align: top;
    height: auto;

  }

  .cocktail-item-good:before {
    position: absolute;
    left: 89.5%;
    top: 20%;
    font-size: 34px;
    content: '  +  ';
    color: #ccc;
  }

  .cocktail-item-good:first-child:before {
    left: 83%;
    content: '=';
  }

  .image {
    width: 100px;
    height: auto;
    position: left;
    display: block;
    margin-left: 110%;
    margin-top: 10%;
    max-width: 100%;
    max-height: 310px;
    min-width: 20px;
    min-height: 20px;
    border-radius: 10px;
    background: #ccc;
  }

  .size {
    display: block;
    margin-top: -60.1%;
    margin-left: 2%;
    max-width: 100%;
    max-height: 310px;
    min-width: 20px;
    min-height: 20px;
    border-radius: 6px;
    background: #ccc;
    float: center;
  }

  .search-results {
    width: 100px;
    margin-top: 110%;
    background: #ccc;
  }
</style>
