<template lang="html">
  <div
    :class="['pixel', color, current ? 'current' : '']"
    @click="handleClick"
  ></div>
</template>

<script>
export default {
  name: "Pixel",
  props: {
    color: String,
    current: Boolean,
    isInColorPicker: Boolean,
    isInCanvas: Boolean,
    index: Number
  },
  methods: {
    handleClick: function() {
      if (this.isInColorPicker) {
        this.$root.$emit("updatecolor", this.color);
      }
      if (this.isInCanvas) {
        this.$root.$emit("clickedpixel", this.index);
      }
    }
  }
};
</script>

<style lang="css" scoped>
.pixel {
  border: 1px solid lightgray;
  width: 30px;
  height: 30px;
  box-sizing:border-box;
}

.white {
  background-color: white;
}
.lightblue {
  background-color: rgb(0, 188, 212);
}
.blue {
  background-color: rgb(3, 169, 244);
}
.darkblue {
  background-color: rgb(33, 150, 243);
}

.red {
  background-color: rgb(255, 0, 0);
}

.black {
  background-color: rgb(0,0,0);
}

.yellow {
  background-color: rgb(255,255,0)
}

.magenta {
  background-color: rgb(255,0,255)
}

.green {
  background-color: rgb(0,128,0)
}
.pixel.current {
  border: 4px solid yellow;
}
</style>
