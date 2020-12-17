<template>
<div>
    <div v-for="item in items" :key="item.message">
        <div class="card1" v-bind:class="item.bp=='0' ? 'glay' : item.color">
            <div class=card-upper-text>{{item.message}}</div>
            <div class=card-lower-text>{{item.bp}}BP</div>
        </div>
    </div>
</div>
</template>

<script>
import { SliderEvent } from '../SliderEvent.js'

let BP_LIST = [
    0,
14000,
13666,
15333,
16333,
16666,
17666,
19000,
26000,
25666,
25666,
21333,
22666,
25666,
29000,
28666,
27666,
26333,
28666,
31333,
30666,
31000,
29333,
31333,
31000,
31333,
32000,
33000,
34333,
37333,
37000,
38333,
36000,
37000,
37333,
38000,
39000,
38666,
39000,
44666,
46333,
48333,
44000,
45000,
48333,
51666,
54666,
54333,
54000,
53000
]

export default {
    name: 'BpTaskCards',
    data () {
        return {
            items: [
                { level:40, message: '40 Level : 3rd teachable perk unlock', bp: '0' , color: "red"},
                { level:35, message: '35 Level : 2nd teachable perk unlock', bp: '0' , color: "pale-red"},
                { level:30, message: '30 Level : 1st teachable perk unlock', bp: '0' , color: "light-red"}
            ],
            level: 1
            
        }            
    } ,

    mounted(){
        SliderEvent.$on('level-change',this.calcBP)
        this.calcBP(this.level)  
    },

    methods: {
        calcBP: function(level){
            this.level = level;
            for (let i = 0; i < 3; i++) {       
                let tempBp = 0;
                for (let j = this.level; j < this.items[i].level; j++){
                        tempBp += BP_LIST[j];
                    }
                    this.items[i].bp = tempBp.toLocaleString();
            }

        }
    }


}
</script>

<style>
    .card1{
        padding: 8px;
        text-align: center;
        margin: 8px;
    }

    .card-upper-text{
        font-size: 16px;
        line-height: 24px;
        text-align: center;
        color: #FFFFFF;
        border-bottom: 1px dotted #FFFFFF;
    }

    .card-lower-text{
        font-style: italic;
        font-weight: bold;
        font-size: 24px;
        line-height: 32px;
        text-align: center;
        color: #FFFFFF;
        padding-top: 8px;
    }

    .red{
        background-color: #DE2829;
    }
    .pale-red{
        background-color: #FD6D6D;
    }
    .light-red{
        background-color: #EB8F8F;
    }
    
    .glay{
        background-color: #767575;
    }
</style>