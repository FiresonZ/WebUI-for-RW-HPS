<template>
    <body class="mdui-drawer-body-left mdui-appbar-with-toolbar mdui-theme-primary-indigo mdui-theme-accent-pink">
        <div class="mdui-appbar mdui-appbar-fixed">
            <div class="mdui-toolbar mdui-color-theme">
                <a href="javascript:" class="mdui-btn mdui-btn-icon mdui-ripple" mdui-drawer="{target: '#drawer'}">
                    <i class="mdui-icon material-icons">menu</i>
                </a>
                <a href="javascript:" class="mdui-typo-headline">RW-HPS WebUI</a>
                <div class="mdui-toolbar-spacer"></div>
                <a href="javascript:location.reload();" class="mdui-btn mdui-btn-icon mdui-ripple">
                    <i class="mdui-icon material-icons">refresh</i>
                </a>
                <a href="javascript:" class="mdui-btn mdui-btn-icon mdui-ripple">
                    <i class="mdui-icon material-icons">more_vert</i>
                </a>
            </div>
        </div>
        <div class="mdui-drawer" id="drawer">
            <ul class="mdui-list">
                <li :class="comName==='index'?active:inactive">
                    <i class="mdui-list-item-icon mdui-icon material-icons">dashboard</i>
                    <a href="" @click.prevent="comName='index'" class="mdui-list-item-content">概览</a>
                </li>
                <li :class="comName==='console'?active:inactive">
                    <i class="mdui-list-item-icon mdui-icon material-icons">code</i>
                    <a href="" @click.prevent="comName='console'" class="mdui-list-item-content">控制台</a>
                </li>
            </ul>
        </div>
        <component :is="comName"></component>
    </body>
</template>

<script>
import index from './components/index.vue'
import console from './components/console.vue'

export default {
  data(){
    return{
      comName: 'index',
      active: 'mdui-list-item mdui-ripple mdui-list-item-active',
      inactive: 'mdui-list-item mdui-ripple'
    }
  },
  components: {
    index,
    console
  }
}
</script>

<style>
@import url(https://cdn.firesonz.top/rwhpswebui/css/mdui.css)
</style>
