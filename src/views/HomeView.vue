<script setup>
import tags from '../components/tags.vue'
import ImputZone from '../components/ImputZone.vue';
</script>

<template>
  <main class=" container">
    <section id="first-section">
      <div id="tags">
        <tags />
      </div>
      <div id="input-zone">
        <ImputZone />
      </div>
    </section>
    <section id="second-section">
      <div id="bear-1">

      </div>
      <div id="bear-2">

      </div>
      <div id="bear-3">

      </div>
      <div id="bear-4">

      </div>
      <div id="bear-5">

      </div>
      <div id="bear-6">

      </div>
    </section>
    <section id="third-section">
        <div id="bear-7">

        </div>
        <div id="bear-8">

        </div>
        <div id="bear-9">

        </div>
      </section>
  </main>
</template>
<style lang="scss" scoped>
@use "sass:math";

//MIXINS
@mixin border($RowInit, $ColumnInit , $RowEnd, $columnEnd) {
  grid-row-start: $RowInit;
  grid-row-end: $RowEnd;
  grid-column-start: $ColumnInit;
  grid-column-end: $columnEnd;
  border: 2px solid;
  margin: 10px;
}

@mixin gridDisplay($FirstArgument, $SecondArgument) {
  display: grid;
  grid-template: repeat($FirstArgument, 1fr) / repeat($SecondArgument, 1fr);
}

//STYLES
.container {
  width: 80%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;

  #first-section {
    width: 100%;
    height: 20%;
    @include gridDisplay(2, 10);

    #tags {
      display: flex;
      align-items: center;
      justify-content: center;
      @include border(1, 1, 3, 6);
    }

    #input-zone {
      display: flex;
      align-items: center;
      justify-content: center;
      @include border(1, 6, 3, 11);

    }
  }

  #second-section {
    width: 100%;
    height: 60%;
    @include gridDisplay(2, 10);

    #bear-1 {
      @include border(1, 1, 1, 3)
    }

    #bear-2 {
      @include border(1, 3, 1, 5)
    }

    #bear-3 {
      @include border(1, 5, 3, 9)
    }

    #bear-4 {
      @include border(1, 9, 1, 11)
    }

    #bear-5 {
      @include border(2, 1, 2, 5)
    }

    #bear-6 {
      @include border(2, 9, 2, 11)
    }
  }
  #third-section {
    width: 100%;
    height: 20%;
    @include gridDisplay(2, 10);
    #bear-7 {
      @include border(1, 1, 3, 3)
    }

    #bear-8 {
      @include border(1, 3, 3, 5)
    }

    #bear-9 {
      @include border(1, 5, 3, 11)
    }
    
  }

}
</style>