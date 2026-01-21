
# Pagination

Pagination details

## Structure

`Pagination`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Page` | `double` | Required | Current page number | double getPage() | setPage(double page) |
| `Limit` | `double` | Required | Items per page | double getLimit() | setLimit(double limit) |
| `Total` | `double` | Required | Total number of items | double getTotal() | setTotal(double total) |
| `TotalPages` | `double` | Required | Total number of pages | double getTotalPages() | setTotalPages(double totalPages) |
| `HasNext` | `boolean` | Required | Has next page | boolean getHasNext() | setHasNext(boolean hasNext) |
| `HasPrev` | `boolean` | Required | Has previous page | boolean getHasPrev() | setHasPrev(boolean hasPrev) |

## Example (as JSON)

```json
{
  "page": 1.8,
  "limit": 128.66,
  "total": 19.52,
  "total_pages": 188.86,
  "has_next": false,
  "has_prev": false
}
```

