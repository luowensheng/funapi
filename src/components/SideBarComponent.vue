<template>
    <aside class="flex-justify-center">

      <div class="tasks-container flex-column invisible-scrollbar">
        
        <TaskListViewComponent :title="task.name" :items="task.items" v-bind:key="index" v-for="(task, index) in tasks"/>

      </div>

    </aside>
</template>

<script>
import TaskListViewComponent from './TaskListViewComponent.vue'

export default {
  name: 'SideBarComponent',
  components: {
    TaskListViewComponent
  },
  data() {
    return {
      tasks: [
        {name: "Getting Started", items: [
          "Introduction"
        ]},
        {name: "Language", items: [
            "Language API",
            "Generate Random Topics",
            "Generate Related Topics",
            "Generate Descriptions of People",
            "Generate Random Conversations",
            "Generate Specific Conversations",
        ]},
        {name: "Visual", items: [
            "Visual API",
            "Generate Pictures of People",
        ]},
      ]
    }
  }
}
</script>

<style scoped>
.tasks-container {
  gap: 30px;
  overflow-y: auto;

}

.tasks-container > * {
  gap: 10px;
}
</style>