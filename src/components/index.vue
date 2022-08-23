<script>

</script>

<template>
    <button class="mdui-fab mdui-color-theme-accent mdui-fab-fixed mdui-ripple mdui-fab-hide" id="fab" mdui-dialog="{target: '#dialog'}">
        <i class="mdui-icon material-icons">add</i>
    </button>

    <div class="mdui-dialog" id="dialog">
        <div class="mdui-dialog-title">设置服务器</div>
        <div class="mdui-dialog-content">
            <div class="mdui-textfield">
                <input class="mdui-textfield-input" placeholder="127.0.0.1:5123" id="ipAddress" type="text"/>
                <div class="mdui-textfield-helper">IP:PORT(服务器必须开启HttpApi)</div>
            </div>
            <div class="mdui-textfield mdui-textfield-floating-label">
                <label class="mdui-textfield-label">Token</label>
                <input class="mdui-textfield-input" type="password" id="token"/>
            </div>
            <input mdui-dialog-confirm class="mdui-btn mdui-btn-raised mdui-ripple mdui-color-theme-accent" type="submit" value="提交" onclick="submit()" />
        </div>
    </div>
    <div class="mdui-container mdui-typo">
        <br>
        <div class="mdui-row">
        </div>
        <component :is="'script'" src="https://cdn.firesonz.top/rwhpswebui/js/index.js" type="text/javascript"></component>
    </div>
</template>

<style>
</style>