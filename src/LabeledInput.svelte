<script>
  export let label;
  export let value;
</script>

<label>
  {label}
  <input bind:value={value}>
</label>
