<template>
  <btn-base class="btn-dashboard" v-bind="$attrs" v-on="$listeners">
    <slot />
  </btn-base>
</template>
<script lang="ts">
export default {
  components: {
    "btn-base": () => import("../el/btn-base.vue"),
  },
}
</script>
<style lang="less">
.factor-dashboard {
  .factor-btn + .factor-btn,
  .btn-link + .factor-btn {
    margin-left: 0.5rem;
  }
}

.btn-dashboard.factor-btn {
  color: var(--color-text);
  transition: 0.15s all;
  opacity: 0.95;
  font-weight: var(--font-weight-bold);
  padding: 0.55em 1em;
  border: none;
  border-radius: 4px;
  background-color: #fff;
  font-size: 1em;
  &:active {
    opacity: 0.8;
    transition: 0s all;
  }

  &:hover {
    opacity: 0.8;
  }

  &.tiny {
    font-size: 11px;
    padding: 2px 4px;
    font-weight: 500;
  }
  &.small {
    font-size: 12px;
    padding: 0.35em 0.75em;
  }
  &.large {
    font-size: 1.2em;
  }

  &.subtle {
    box-shadow: none;
    opacity: 0.6;
  }

  &.default {
    box-shadow: inset var(--box-shadow-input);
  }

  &.primary {
    color: #fff;
    background: var(--color-primary);

    &:hover {
      color: #fff;
    }
  }
  &.secondary {
    color: #fff;
    background: var(--color-secondary);

    &:hover {
      color: #fff;
    }
  }
  &.warning {
    color: #fff;
    background: var(--color-warning);

    &:hover {
      color: #fff;
    }
  }
}
</style>
