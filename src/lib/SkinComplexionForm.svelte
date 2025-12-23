<script lang="ts">
  let color = $state("#f5e0d3");
</script>

<div class="flex flex-col w-full gap-2.5">
  <label for="color">Skin Complexion: {color}</label>
  <input bind:value={color} type="color" name="color" id="color" />
</div>
