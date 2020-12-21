<template>
  <log-event-source :id="id" v-slot="eventSource" @loading-more="$emit('loading-more', $event)">
    <log-viewer :messages="eventSource.messages"></log-viewer>
  </log-event-source>
</template>

<script lang="ts">
import LogEventSource from "@/components/LogEventSource.vue";
import LogViewer from "@/components/LogViewer.vue";

export default {
  props: ["id"],
  name: "LogViewerWithSource",
  components: {
    LogEventSource,
    LogViewer,
  },
};
</script>
