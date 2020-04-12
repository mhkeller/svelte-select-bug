<script>

  let clientWidth = 0;
  let clientHeight = 0;
</script>

<div class="block-component"
  bind:clientWidth
  bind:clientHeight
>
<!-- <span>{clientWidth}x{clientHeight}</span> -->
<svg
  width={clientWidth}
  height={clientHeight}
>
  <text x="0" y="20">{clientWidth}x{clientHeight}</text>
</svg>
</div>

<style>
  .block-component {
    width: 100%;
    height: 100%;
    background-color: #fc0;
  }
  span, svg {
    top: 0;
    left: 0;
    position: absolute;
  }
</style>
