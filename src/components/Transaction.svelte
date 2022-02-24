<script>
  export let mode;
  export let value;

  $: cssClass = getCssClass(mode);
  const getCssClass = (mode) => {
    switch (mode) {
      case 'balance':
        return 'is-info';
      case 'income':
        return 'is-success';
      case 'expenses':
        return 'is-danger';
    }
  };
</script>

<div class="notification {cssClass} is-light has-text-left">
  {value}
</div>
