# TanStack Table (react table) pagination

## TanStack Table (react table) server side pagination example [demo](https://codesandbox.io/p/devbox/tanstack-table-react-table-pagination-8qfzhj?layout=%257B%2522sidebarPanel%2522%253A%2522EXPLORER%2522%252C%2522rootPanelGroup%2522%253A%257B%2522direction%2522%253A%2522horizontal%2522%252C%2522contentType%2522%253A%2522UNKNOWN%2522%252C%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522id%2522%253A%2522ROOT_LAYOUT%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522UNKNOWN%2522%252C%2522direction%2522%253A%2522vertical%2522%252C%2522id%2522%253A%2522clq0plp9o000a356k0oi0bb4n%2522%252C%2522sizes%2522%253A%255B70%252C30%255D%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522EDITOR%2522%252C%2522direction%2522%253A%2522horizontal%2522%252C%2522id%2522%253A%2522EDITOR%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522EDITOR%2522%252C%2522id%2522%253A%2522clq0plp9m0002356kuitv6xps%2522%257D%255D%257D%252C%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522SHELLS%2522%252C%2522direction%2522%253A%2522horizontal%2522%252C%2522id%2522%253A%2522SHELLS%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522SHELLS%2522%252C%2522id%2522%253A%2522clq0plp9n0007356kfjsy64cu%2522%257D%255D%252C%2522sizes%2522%253A%255B100%255D%257D%255D%257D%252C%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522DEVTOOLS%2522%252C%2522direction%2522%253A%2522vertical%2522%252C%2522id%2522%253A%2522DEVTOOLS%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522DEVTOOLS%2522%252C%2522id%2522%253A%2522clq0plp9n0009356kq0b8b5j4%2522%257D%255D%252C%2522sizes%2522%253A%255B100%255D%257D%255D%252C%2522sizes%2522%253A%255B50%252C50%255D%257D%252C%2522tabbedPanels%2522%253A%257B%2522clq0plp9m0002356kuitv6xps%2522%253A%257B%2522id%2522%253A%2522clq0plp9m0002356kuitv6xps%2522%252C%2522tabs%2522%253A%255B%255D%257D%252C%2522clq0plp9n0009356kq0b8b5j4%2522%253A%257B%2522id%2522%253A%2522clq0plp9n0009356kq0b8b5j4%2522%252C%2522tabs%2522%253A%255B%257B%2522id%2522%253A%2522clq0plp9n0008356k7gx9wjth%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522TASK_PORT%2522%252C%2522taskId%2522%253A%2522dev%2522%252C%2522port%2522%253A5173%252C%2522path%2522%253A%2522%252F%2522%257D%255D%252C%2522activeTabId%2522%253A%2522clq0plp9n0008356k7gx9wjth%2522%257D%252C%2522clq0plp9n0007356kfjsy64cu%2522%253A%257B%2522tabs%2522%253A%255B%257B%2522id%2522%253A%2522clq0plp9n0003356k05tjiolg%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522TASK_LOG%2522%252C%2522taskId%2522%253A%2522dev%2522%257D%252C%257B%2522id%2522%253A%2522clq0plp9n0004356k79hz3ijm%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522TASK_LOG%2522%252C%2522taskId%2522%253A%2522build%2522%257D%252C%257B%2522id%2522%253A%2522clq0plp9n0005356kht38sqwk%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522TASK_LOG%2522%252C%2522taskId%2522%253A%2522serve%2522%257D%252C%257B%2522id%2522%253A%2522clq0plp9n0006356kzfn6yabp%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522TASK_LOG%2522%252C%2522taskId%2522%253A%2522start%2522%257D%255D%252C%2522id%2522%253A%2522clq0plp9n0007356kfjsy64cu%2522%252C%2522activeTabId%2522%253A%2522clq0plp9n0003356k05tjiolg%2522%257D%257D%252C%2522showDevtools%2522%253Atrue%252C%2522showShells%2522%253Atrue%252C%2522showSidebar%2522%253Atrue%252C%2522sidebarPanelSize%2522%253A15%257D)

Api end point we are using for this example is https://jsonplaceholder.typicode.com/posts?_start=0&_limit=10

We can use \_start and \_limit url parameters to fetch sample data from api.
This is the pagination properties we are providing for useReactTable.

```typescript
const [{ pageIndex, pageSize }, setPagination] = useState<PaginationState>({
  pageIndex: 0,
  pageSize: 10,
});
```

Table will update the page size and page index,so we are going listen changes and update table data.

```typescript
const [tblData, setTblData] = useState<Array<Post>>([]);
const [total, setTotal] = useState(0);

const getPageData = (page: number, size: number) => {
  fetch(
    "https://jsonplaceholder.typicode.com/posts?_start=${page}&_limit=${size}"
  )
    .then((response) => {
      console.log(response.headers.get("X-Total-Count"));
      setTotal(Number.parseInt(response.headers.get("X-Total-Count") ?? "0"));
      return response.json();
    })
    .then((json) => setTblData(json as Array<Post>));
};

useEffect(() => {
  getPageData(pageIndex, pageSize);
}, [pageIndex, pageSize]);
```
