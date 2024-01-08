<!-- ThemeSwitch.svelte -->
<script>
  import { theme } from '$lib/stores';
</script>

<select bind:value="{$theme}">
  <option value="light">light</option>
  <option value="dark">dark</option>
</select>
