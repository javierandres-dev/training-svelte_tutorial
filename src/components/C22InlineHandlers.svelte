<script>
  const move = { x: 0, y: 0 };
</script>

<div
  on:mousemove={(e) => {
    (move.x = e.clientX), (move.y = e.clientY);
  }}
>
  The mouse position is {move.x} x {move.y}
</div>

<style>
  div {
    width: 300px;
    height: 150px;
    background-color: yellow;
    text-align: center;
  }
</style>
