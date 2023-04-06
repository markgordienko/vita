<template>
  <div>
    <div class="cards-wrapper">
      <card-component
        :data="note"
        v-for="note in notes"
        :key="note.noteId"
      />
    </div>
  </div>
</template>

<script>
import CardComponent from '../CardComponent/CardComponent.vue'

export default {
  components: { CardComponent },
  name: 'MainComponent',
  data () {
    return {
      notes: [
        { header: 'Заметка 1', memos: 'нотсы', noteId: 1 },
        { header: 'Заметка 2', memos: 'нотсы', noteId: 2 },
        { header: 'Заметка 3', memos: 'нотсы', noteId: 3 },
        { header: 'Заметка 4', memos: 'нотсы', noteId: 4 },
        { header: 'Заметка 5', memos: 'нотсы', noteId: 5 },
        { header: 'Заметка 6', memos: 'нотсы', noteId: 6 },
        { header: 'Заметка 7', memos: 'нотсы', noteId: 7 },
        { header: 'Заметка 8', memos: 'нотсы', noteId: 8 },
        { header: 'Заметка 9', memos: 'нотсы', noteId: 9 },
        { header: 'Заметка 10', memos: 'нотсы', noteId: 10 },
        { header: 'Заметка 11', memos: 'нотсы', noteId: 11 },
        { header: 'Заметка 12', memos: 'нотсы', noteId: 12 },
        { header: 'Заметка 13', memos: 'нотсы', noteId: 13 },
        { header: 'Заметка 14', memos: 'нотсы', noteId: 14 },
        { header: 'Заметка 15', memos: 'нотсы', noteId: 15 },
        { header: 'Заметка 16', memos: 'нотсы', noteId: 16 }
      ]
    }
  }
}
</script>

<style scoped>
.cards-wrapper {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: start;
  -ms-flex-align: start;
  align-items: flex-start;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  padding: 50px 0;
}
</style>
