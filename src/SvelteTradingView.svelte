<script>
  import { onMount } from "svelte";
  export let options = Object;
  const SCRIPT_ID = "tradingview-widget-script";
  const CONTAINER_ID = "svelte-trading-view";

  onMount(() => {
    appendScript(initWidget);
  });

  function canUseDOM() {
    return (
      typeof window !== "undefined" &&
      window.document &&
      window.document.createElement
    );
  }

  function getScriptElement() {
    return document.getElementById(SCRIPT_ID);
  }

  function updateOnloadListener(onload) {
    const script = getScriptElement();
    const oldOnload = script.onload;
    return (script.onload = () => {
      oldOnload();
      onload();
    });
  }

  function scriptExists() {
    return getScriptElement() !== null;
  }

  function appendScript(onload) {
    if (!canUseDOM()) {
      onload();
      return;
    }

    if (scriptExists()) {
      if (typeof TradingView === "undefined") {
        this.updateOnloadListener(onload);
        return;
      }
      onload();
      return;
    }
    const script = document.createElement("script");
    script.id = SCRIPT_ID;
    script.type = "text/javascript";
    script.async = true;
    script.src = "https://s3.tradingview.com/tv.js";
    script.onload = onload;
    document.getElementsByTagName("head")[0].appendChild(script);
  }

  function initWidget() {
    if (typeof TradingView === "undefined") {
      return;
    }

    new window.TradingView.widget(Object.assign(CONTAINER_ID, options));
  }
</script>

<div id={CONTAINER_ID} />
