<template>
  <div class="list-container">
  <i @click="scrollLeft" class="fa fa-chevron-left" aria-hidden="true"></i>
  <ul id="list">
    <li :key="option" v-for="option in options">
      {{ option }}
    </li>
  </ul>
  <i @click="scrollRight" class="fa fa-chevron-right" aria-hidden="true"></i>
</div>
</template>

<script>
export default {
  name: 'ScrollNav',
  data: () => {},
  props: {
    options: Array,
  },
  methods: {
    scrollLeft(e) {
      e.preventDefault();
      const scroller = document.getElementById('list');
      const currentScrollValue = scroller.scrollLeft
      scroller.scrollLeft += 200
      this.disableScrollIcon('left', currentScrollValue)
    },
    scrollRight(e) {
      e.preventDefault();
      const scroller = document.getElementById('list');
      const currentScrollValue = scroller.scrollLeft
      scroller.scrollLeft -= 200
      this.disableScrollIcon('right', currentScrollValue)
    },
    disableScrollIcon(side, compare) {
      const scroller = document.getElementById('list');
      const otherSide = side === 'left' ? 'right' : 'left'
      const currentScrollValue = scroller.scrollLeft
      if((side === 'right' && compare === currentScrollValue && compare === 0) ||
       (side === 'left' && compare === currentScrollValue && compare !== 0)) {
        document.getElementsByClassName(`fa-chevron-${side}`)[0].classList.add('disabled')
        document.getElementsByClassName(`fa-chevron-${otherSide}`)[0].classList.remove('disabled')
      } else {
        document.getElementsByClassName('fa')[0].classList.remove('disabled')
        document.getElementsByClassName('fa')[0].classList.remove('disabled')
      }
    }
  }
}
</script>

<style scoped>
  li {
    list-style-type: none;
    padding: 0px 10px;
  }

  .disabled {
    opacity: 0.2
  }


  ul {
    display: flex;
    overflow: scroll;
    scroll-behavior: smooth;
  }

  ul::-webkit-scrollbar {
    width: 0px;
    height: 0px;
  }
 

  i {
    color: inherit;
    justify-items: center;
    cursor: pointer;
    padding: 0px 10px;
  }

  .list-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>