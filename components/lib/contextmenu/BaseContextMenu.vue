<script>
import BaseComponent from 'primevue/basecomponent';
import ContextMenuStyle from 'primevue/contextmenu/style';

export default {
    name: 'BaseContextMenu',
    extends: BaseComponent,
    props: {
        model: {
            type: Array,
            default: null
        },
        appendTo: {
            type: String,
            default: 'body'
        },
        autoZIndex: {
            type: Boolean,
            default: true
        },
        baseZIndex: {
            type: Number,
            default: 0
        },
        global: {
            type: Boolean,
            default: false
        },
        tabindex: {
            type: Number,
            default: 0
        },
        ariaLabelledby: {
            type: String,
            default: null
        },
        ariaLabel: {
            type: String,
            default: null
        }
    },
    style: ContextMenuStyle,
    provide() {
        return {
            $parentInstance: this
        };
    }
};
</script>
