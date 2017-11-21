<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <div class="echarts-container">
      <ul>
        <li>
          <router-link to='/' tag='a'>饼图</router-link>
        </li>
        <li>
          <router-link to='/line' tag='a'>折线图</router-link>
        </li>
      </ul>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.echarts-container {

}
.echarts-container ul {
  width: auto;
  overflow: hidden;
  border-bottom: 1px solid #dedede;
  padding-bottom: 20px;
}
.echarts-container ul li {
  width: auto;
  float: left;
  margin-left: 20px;
  list-style: none;
}
.echarts-container ul li a {
  color: #333;
  text-decoration: none;
}
</style>
