<template>
    <div class="taskview">
        <div>{{this.title}}</div>
        <div class="pointer" v-bind:key="index" v-for="(item, index) in items">{{ item }}</div>
    </div>
</template>

<script>
export default {
  name: 'TaskListViewComponent',
  props: ["title", "items"],
  components: {
  }
}
</script>

<style scoped>
.taskview {
    color: rgb(119, 119, 119);
    text-align: left;
    font-weight: 500;
}

.pointer:hover {
    color: black;
}
.taskview>div {
    margin-top: 10px;
}

.taskview>div:nth-child(1) {
    font-weight: 600;
    color: black;
}

</style>