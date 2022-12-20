<page>
    <actionBar title="NativeFlix" />
    <stackLayout>
        <listView height="100%" separatorColor="transparent" items="{flicks}">
            <Template let:item>
                <label text="{item.title}" />
            </Template>
        </listView>
    </stackLayout>
</page>

<script lang="ts">
    import { Template } from 'svelte-native/components'
    import { FlickService } from '../services/FlickService'

    let flicks = FlickService.getInstance().getFlicks()
</script>

<style>
    /* .info {
        font-size: 20;
    } */
</style>
