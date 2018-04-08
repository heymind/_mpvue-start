<template>
<div class="lesson-card">
    <div class="lesson-card-header">
        <p class="lesson-card-title">{{classTitle}}</p>
        <p class="lesson-card-title-small">{{peopleCount}}人</p>
        <div class="lesson-card-title-spacer"></div>
        <p class="lesson-card-title-right">{{point}}学分</p>
    </div>
    <div class="lesson-card-content">
        <p class="lesson-card-content-label">教师</p>
        <p class="lesson-card-content-value">{{teachers}}</p>
        <div class="lesson-card-content-spacer"></div>
        <p class="lesson-card-content-label">学期</p>
        <p class="lesson-card-content-value">{{term}}</p>
    </div>
    <div class="lesson-card-footer">
        <p>作业</p>
        <p class="lesson-card-p-big">{{hwFinished}}</p>
        <p>未交</p>
        <p class="lesson-card-p-big">{{hwUnFinished}}</p>
        <p>已交</p>
    </div>
</div>
</template>

<script>
export default {
  props: {
    classTitle:String,
    peopleCount:Number,
    point:Number,
    teachers:String,
    term:String,
    hwFinished:Number,
    hwUnFinished:Number
  }
}
</script>

<style>
.lesson-card {
    margin:0.5em;
    padding:0.5em;
    width:90%;
    box-shadow: 0 2px 2px 0 rgba(0,0,0,.14), 0 3px 1px -2px rgba(0,0,0,.2), 0 1px 5px 0 rgba(0,0,0,.12);
    display:flex;
    flex-flow:column nowrap;
    justify-content: space-around;
    align-items:stretch;
}
.lesson-card-header{
    padding:.4em;
    display:flex;
    flex-flow:row nowrap;
    justify-content: space-between;
    align-items:baseline;
}
.lesson-card-title-spacer{
    flex-grow:1;
}
.lesson-card-title{
    font-size:1.5em;
}
.lesson-card-title-small{
    margin-left:0.25em;
    font-size:0.75em;
    color:#999;
}
.lesson-card-title-right{
    font-size:1.5em;
    color:#888;
}
.lesson-card-content{
    padding:.4em;
    display:flex;
    flex-flow:row nowrap;
    justify-content: space-between;
}
.lesson-card-content-spacer{
    flex-grow:1;
}
.lesson-card-content-label{
    padding:.2em;
    color:#888;
}
.lesson-card-content-value{
    padding:.2em;
}
.lesson-card-footer{
    padding:0 .4em;
    display:flex;
    flex-flow:row nowrap;
    justify-content: flex-end;
    align-items:baseline;
    color:#888;
}
.lesson-card-text-big{
    margin:0 0.5em;
    font-size:1.5em;
    color:#000 !important;
}
</style>
