<script>
  import { getContext } from "svelte"
  import Table from "../components/Table.svelte";
  export let search
  export let resultPage
  export let pagination
  export let parSearchableColumns
  export let dataProvider
  export let parRowsPerPage
  export let parSortOrder
  export let parSortBy
  export let columns
  export let tableEvent
  export let searchableColumns

  const { styleable } = getContext("sdk")
  const component = getContext("component")
</script>

<div use:styleable={$component.styles}>
  <Table dataProvider={dataProvider} search={search} resultPage={resultPage} pagination={pagination} searchableColumns={searchableColumns} parRowsPerPage={parRowsPerPage} parSortOrder={parSortOrder} columns={columns} parSortBy={parSortBy} tableEvent={tableEvent} />
</div>
