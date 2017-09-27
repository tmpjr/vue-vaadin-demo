<template>
  <div class="data-grid">
    <h3>{{ title }}</h3>
    <link rel="import" href="static/bower_components/vaadin-grid/vaadin-grid.html">
    <vaadin-grid items='[{"name": "John", "surname": "Lennon", "role": "singer"},
      {"name": "Ringo", "surname": "Starr", "role": "drums"}]'>
        <vaadin-grid-column>
          <template class="header">Name</template>
          <template>[[item.name]]</template>
        </vaadin-grid-column>
        <vaadin-grid-column>
          <template class="header">Surname</template>
          <template>[[item.surname]]</template>
        </vaadin-grid-column>
        <vaadin-grid-column>
          <template class="header">Role</template>
          <template>[[item.role]]</template>
        </vaadin-grid-column>
      </vaadin-grid>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: "Vaadin/Vue Grid"
    }
  }
}
</script>