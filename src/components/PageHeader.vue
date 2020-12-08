<template>
    <div class="page_header">
        <div class="left_header">
            <div class="page_title">DbD BP Counter</div>
        </div>
        <div class="right_header">
            <div class="ver_text">ver {{ver_no}}</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'PageHeader',
  data () {
    return {
      ver_no: '0.0.1'
    }
  }
}
</script>

<style scoped>
.page_header {
    display: flex;
    background-color: #1F2020;
    height: 42px;
    justify-content: space-between;
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 500;
}

.page_title {
    font-size: 18px;
    line-height: 42px;
    font-family: Roboto;
    font-style: normal;
    font-weight: 900;
    color: #B4B4B4;
}

.left_header {
    padding-left: 8px;
}

.right_header {
    background: #DE2829;
    padding: 0px 16px;
}

.ver_text {
    color: #FFFFFF;
    line-height: 42px;
    font-size: 12px;
}

</style>
