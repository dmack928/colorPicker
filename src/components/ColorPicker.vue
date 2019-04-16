<template lang="html">
  <div>
    <Pixel
      isInColorPicker
      color="white"
      :current="color == 'white' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="lightblue"
      :current="color == 'lightblue' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="blue"
      :current="color == 'blue' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="darkblue"
      :current="color == 'darkblue' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="red"
      :current="color == 'red' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="black"
      :current="color == 'black' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="yellow"
      :current="color == 'yellow' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="magenta"
      :current="color == 'magenta' ? true : false"
    />
    <Pixel
      isInColorPicker
      color="green"
      :current="color == 'green' ? true : false"
    />
  </div>
</template>

<script>
import Pixel from "./Pixel";

export default {
  name: "ColorPicker",
  props: {
    color: String
  },
  methods: {
    changeColor: function(color) {
      alert(color);
    }
  },
  components: {
    Pixel
  }
};
</script>

<style lang="css" scoped></style>
