<template>
    <div class="backdrop">

    <div class="modal">
    <h1>{{ heading }}</h1>
    <p>Modals are pop-ups used to pass an information and are triggered by an event</p>
    </div>
    </div>
  
  
</template>

<script>
export default {
  name: 'Modal',
  props: [heading],
  data() {
    return {

    }
  }
}
</script>

<style>
.backdrop {
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    align-items: start;
    justify-content: center;
    background: rgba(0, 0, 0, 0.5);
}

.modal {
    padding: 2rem;
    background: white;
    color: black;
    border-radius: 5px;
    width: 300px;
    }

</style>