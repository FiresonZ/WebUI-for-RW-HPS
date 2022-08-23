<script>
</script>

<template>
    <div class="mdui-container mdui-typo">
        <br>
        <div class="mdui-row">
            <pre style="white-space: pre-line;overflow: auto;" id="point">
            </pre>
            <div class="mdui-textfield">
                <label for="command"></label>
                <input class="mdui-textfield-input" type="text" id="command" />
            </div>
        </div>
        <component :is="'script'" src="https://cdn.firesonz.top/rwhpswebui/js/console.js" type="text/javascript"></component>
    </div>
</template>

<style>
</style>