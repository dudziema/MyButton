<template>
  <v-btn v-bind="$attrs">
    <template #prepend>
      <slot name="prepend"></slot>
    </template>

    <slot></slot>

    <template #append>
      <slot name="append"></slot>
    </template>
  </v-btn>
</template>
