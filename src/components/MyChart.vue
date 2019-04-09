<template>
    <div class="mychart"></div>
</template>

<script>
    import echarts from 'echarts'

    export default {
        props:['chartType','chartDimensions','chartDatasetSource'],
        data(){
            return {
                chart:null,
                option:{
                    color : ["#008080","#2d8fc0","#2d8fc0","#2d8fc0","#2d8fc0","#2d8fc0","#2d8fc0"],
                    grid: {left:60, right:60, top:60, bottom:60 },
                    legend : {top:20},
                    tooltip : {},
                    dataset : {
                        dimensions:eval(this.chartDimensions),
                        source:eval(this.chartDatasetSource)
                    },
                    xAxis : [{type : 'category' } ],
                    yAxis : [{type : 'value'} ],
                    series : (()=>{
                        var series = new Array(Object.keys(eval(this.chartDatasetSource)[0]).length-1);
                        series.fill({type:this.chartType});
                        return series;
                    })()
                }
            }
        },
        created(){
            console.info("created...");
        },
        mounted(){
            console.info("mounted...");
            this.chart = echarts.init(this.$el);
            this.chart.setOption(this.option,true);
        },
        updated(){
            console.info("updated...");
        },
        watch:{
            option:{
                handler(){
                    this.chart.setOption(nval);
                },
                deep:true,
                imediate:false
            }
        }
    }
</script>

<style scoped>
    .mychart{width:100%;height:100%;overflow:hidden;}
</style>