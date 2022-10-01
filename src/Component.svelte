<script>
  import { getContext } from "svelte"
  import QrCode from "svelte-qrcode"

  export let text

  const { styleable } = getContext("sdk")
  const component = getContext("component")
</script>

<div use:styleable={$component.styles}>
  <QrCode value={text} />
</div>
