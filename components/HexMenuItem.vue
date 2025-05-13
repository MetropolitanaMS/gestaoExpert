<template>
  <svg
    viewBox="-1 -0.866 2 1.732"
    class="hex-menu-item"
    preserveAspectRatio="xMidYMid meet"
    :style="{
      '--item-color': isSelected ? selectedColor : color,
      '--hover-color': hoverColor,
      '--text-color': textColor,
    }"
    :class="{ selected: isSelected }"
  >
    <polygon
      class="hex"
      points="1,0 0.5,0.866 -0.5,0.866 -1,0 -0.5,-0.866 0.5,-0.866"
    />
    <text
      class="rotate-270"
      text-anchor="middle"
      alignment-baseline="central"
      fill="var(--text-color)"
      font-size="0.2"
    >
      {{ label }}
    </text>
  </svg>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: "#6c6",
    },
    hoverColor: {
      type: String,
      default: "#69c",
    },
    isSelected: {
      type: Boolean,
      default: false,
    },
    selectedColor: {
      type: String,
      default: "#ff6347",
    },
    textColor: {
      type: String,
      default: "#fff",
    },
  },
};
</script>

<style scoped>
.hex-menu-item {
  transition: fill 500ms ease;
}

.hex {
  fill: var(--item-color);
  pointer-events: auto;
  z-index: -1;
  backface-visibility: hidden;
  width: fit-content;
}

.hex-menu-item:hover .hex:not(.selected) {
  fill: var(--hover-color);
}

.hex-menu-item.selected .hex {
  fill: var(--item-color);
}
</style>
