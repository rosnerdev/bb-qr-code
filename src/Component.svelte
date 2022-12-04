<script>
  import { getContext } from "svelte"
  import QrCode from "svelte-qrcode"

  export let text
  export let size
  export let color
  export let backgroundColor
  export let padding

  const { styleable } = getContext("sdk")
  const component = getContext("component")
</script>

<div use:styleable={$component.styles}>
  <QrCode value={text} size={size} color={color} background={backgroundColor} padding={padding} />
</div>
