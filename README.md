# el-tab-closable-useless
el-tab closable与editable冲突问题
源码位置node_modules/element-ui/packages/tabs/src/tab-nav.vue
const tabs = this._l(panes, (pane, index) => {
        let tabName = pane.name || pane.index || index;
        // const closable = pane.isClosable !== false || editable;
		const closable = pane.isClosable !== false && editable;
        pane.index = `${index}`;

        const btnClose = closable
