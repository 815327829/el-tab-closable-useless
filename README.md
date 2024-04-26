# el-tab-closable-useless
el-tab closable与editable冲突问题
源码位置node_modules/element-ui/packages/tabs/src/tab-nav.vue
const tabs = this._l(panes, (pane, index) => {
        let tabName = pane.name || pane.index || index;
        // const closable = pane.isClosable !== false || editable;
		const closable = pane.isClosable !== false && editable;
        pane.index = `${index}`;


html记得配置closable属性
<el-tab-pane :key="item.name" v-for="(item, index) in editableTabs" :label="item.title":name="item.name" :closable="item.closable"></el-tab-pane>
