<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <charts :options="datas"></charts>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      title: '优翔部门职能环形图',
      datas : {
        tooltip: {
            trigger: 'item',
            formatter: "{a} <br/>{b}: {c} ({d}%)"
        },
        legend: {
            orient: 'vertical',
            x: 'left',
            data:['市场部','IT部','产品部','营销部','其他']
        },
        series: [
            {
                name:'职能占比',
                type:'pie',
                selectedMode: 'single',
                radius: [0, '30%'],

                label: {
                    normal: {
                        position: 'inner'
                    }
                },
                labelLine: {
                    normal: {
                        show: false
                    }
                },
                data:[
                    {value:335, name:'市场部', selected:true},
                    {value:679, name:'IT部'},
                    {value:1548, name:'产品部'},
                    {value:1548, name:'营销部'},
                    {value:1548, name:'其他'}
                ]
            },
            {
                name:'信息占比',
                type:'pie',
                radius: ['40%', '55%'],
                label: {
                    normal: {
                        formatter: '{a|{a}}{abg|}\n{hr|}\n  {b|{b}：}{c}  {per|{d}%}  ',
                        backgroundColor: '#eee',
                        borderColor: '#aaa',
                        borderWidth: 1,
                        borderRadius: 4,
                        // shadowBlur:3,
                        // shadowOffsetX: 2,
                        // shadowOffsetY: 2,
                        // shadowColor: '#999',
                        // padding: [0, 7],
                        rich: {
                            a: {
                                color: '#999',
                                lineHeight: 22,
                                align: 'center'
                            },
                            // abg: {
                            //     backgroundColor: '#333',
                            //     width: '100%',
                            //     align: 'right',
                            //     height: 22,
                            //     borderRadius: [4, 4, 0, 0]
                            // },
                            hr: {
                                borderColor: '#aaa',
                                width: '100%',
                                borderWidth: 0.5,
                                height: 0
                            },
                            b: {
                                fontSize: 16,
                                lineHeight: 33
                            },
                            per: {
                                color: '#eee',
                                backgroundColor: '#334455',
                                padding: [2, 4],
                                borderRadius: 2
                            }
                        }
                    }
                },
                data:[
                    {value:335, name:'市场部'},
                    {value:310, name:'IT部'},
                    {value:234, name:'产品部'},
                    {value:135, name:'营销部'},
                    {value:1048, name:'其他'}
                ]
            }
        ]
      }
    }
  },
  created () {

  },
  components : {
    charts: require('vue-echarts')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.echarts{
  width: 1000px;
}
</style>
