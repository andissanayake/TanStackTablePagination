# TanStack Table (react table) pagination

## TanStack Table (react table) server side pagination example

Api end point we are using for this example is https://jsonplaceholder.typicode.com/posts?_start=0&_limit=10

We can use \_start and \_limit url parameters to fetch sample data from api
This is the pagination properties we are providing for useReactTable.

```typescript
const [{ pageIndex, pageSize }, setPagination] = useState<PaginationState>({
  pageIndex: 0,
  pageSize: 10,
});
```

Table it set will update the page size and page index,so we are going listen changes and update table.

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
