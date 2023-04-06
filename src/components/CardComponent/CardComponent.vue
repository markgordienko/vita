<template>
  <div class="card">
    <div class="card-wrapper">
      <div class="curtain" />
      <div class="card-header">
        {{ data.header }}
      </div>

      <div class="card-body">
        <span class="notes">
          {{ data.memos }}
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object
  },
  name: 'CardComponent',
  data () {
    return {}
  }
}
</script>

<style scoped>

.card {
  -ms-flex-preferred-size: calc(33.33333% - 30px);
  flex-basis: calc(33.33333% - 30px);
  margin: 0 15px 30px;
  overflow: hidden;
  border-radius: 28px;
  cursor: pointer;
}

.card-wrapper {
  display: block;
  padding: 30px 20px;
  background-color: #121212;
  text-decoration: none;
  overflow: hidden;
  position: relative;
}

.card-wrapper:hover,
.card-wrapper:hover .notes {
  text-decoration: none;
  color: #fff;
}

.card-wrapper:hover .curtain {
  -webkit-transform: scale(10);
  -ms-transform: scale(10);
  transform: scale(10);
}

.card-header {
  min-height: 50px;
  margin: 0 0 15px;
  overflow: hidden;
  font-weight: bold;
  font-size: 30px;
  color: #fff;
  z-index: 2;
  position: relative;
}

.card-body {
  max-height: 150px;
  font-size: 18px;
  color: #fff;
  z-index: 2;
  position: relative;
}

.notes {
  font-weight: bold;
  color: #f9b234;
  -webkit-transition: color 0.5s ease;
  -o-transition: color 0.5s ease;
  transition: color 0.5s ease;
}

.curtain {
  height: 128px;
  width: 128px;
  background-color: #f9b234;
  z-index: 1;
  position: absolute;
  top: -75px;
  right: -75px;
  border-radius: 50%;
  -webkit-transition: all 0.5s ease;
  -o-transition: all 0.5s ease;
  transition: all 0.5s ease;
}

.card:nth-child(2n) .curtain {
  background-color: #3ecd5e;
}

.card:nth-child(3n) .curtain {
  background-color: #e44002;
}

.card:nth-child(4n) .curtain {
  background-color: #952aff;
}

.card:nth-child(5n) .curtain {
  background-color: #cd3e94;
}

.card:nth-child(6n) .curtain {
  background-color: #4c49ea;
}

@media only screen and (max-width: 979px) {
  .card {
    -ms-flex-preferred-size: calc(50% - 30px);
    flex-basis: calc(50% - 30px);
  }

  .card-header {
    font-size: 24px;
  }
}

@media only screen and (max-width: 639px) {
  .card {
    -ms-flex-preferred-size: 100%;
    flex-basis: 100%;
  }

  .card-header {
    min-height: 72px;
    line-height: 1;

    font-size: 24px;
  }

  .card-wrapper {
    padding: 22px 40px;
  }

  .card-body {
    font-size: 16px;
  }
}
</style>
