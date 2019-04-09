<template>
    <div class="mychart"></div>
</template>

<script>
    import echarts from 'echarts'
    import { addListener, removeListener } from 'resize-detector'

    export default {
        props:{
            'chartType':{
                required:false,
                type:String,
                default:'bar'
            },
            'chartDimensions':{
                required:false,
                type:Array,
                default:[]
            },
            'chartDatasetSource':{
                required:false,
                type:Array,
                default:[]
            }
        },
        data(){
            return {
                chart:null,
                option:{
                    color : ["#008080","#2d8fc0","#2d8fc0","#2d8fc0","#2d8fc0","#2d8fc0","#2d8fc0"],
                    grid: {left:60, right:60, top:60, bottom:60 },
                    legend : {top:20},
                    tooltip : {},
                    dataset : {
                        dimensions : this.chartDimensions,
                        source : this.chartDatasetSource
                    },
                    xAxis : [{type : 'category' } ],
                    yAxis : [{type : 'value'} ],
                    series : (()=>{
                        var series = new Array(Object.keys(this.chartDatasetSource[0]).length-1);
                        series.fill({type:this.chartType});
                        return series;
                    })()
                }
            }
        },
        created(){

        },
        mounted(){
            this.chart = echarts.init(this.$el);
            this.chart.setOption(this.option,true);

            addListener(this.$el, this.onResize)
        },
        updated(){

        },
        methods:{
            onResize(){
                this.chart.resize();
            }
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