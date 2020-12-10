<template>
<div>
    <div v-for="item in items" :key="item.message">
        <div class="card1">
            <div class=card-upper-text>{{item.message}}</div>
            <div class=card-lower-text>{{item.bp}}BP</div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'BpTaskCards',
    data () {
        return {
            items: [
            { message: '40 Level : 3rd teachable perk unlock',bp: '420,521' },
            { message: '35 Level : 2nd teachable perk unlock',bp: '198,213' },
            { message: '30 Level : 1st teachable perk unlock',bp: '0' }
            ]
        }
    } 
}
</script>

<style>
    .card1{
        background-color: #DE2829;
        padding: 8px;
        text-align: center;
        width: 320px;
        margin-bottom: 8px;
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
</style>