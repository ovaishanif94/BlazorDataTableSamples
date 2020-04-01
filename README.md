# Blazor Data Table
Blazorized Server Side Customized Data Table Component with Pager and Pagination.

### Download or Install
The latest stable release is available on NuGet: https://www.nuget.org/packages/BlazorDataTable/

`Install-Package BlazorDataTable -Version 2.0.0`

## Pager
    <BlazorTablePager Class="" PageSizeChangeEvent="PageSizeChange" PageSizes="new int[] { 25, 50, 100 }" />
    
    @code {
        private async Task PageSizeChange(int pageSize)
        {
            // code
        }
    }

## Pagination
    <BlazorTablePagination PageChangeEvent="PageChange"
        Class=""
        DisplayTotals="false"
        PagingSize="10"
        ActivePage="1"
        PageSize="25"
        NoOfItems="9999" />
    
    @code {
        private async Task PageChange(int page)
        {
            // code
        }
    }
    
## Table
    <BlazorTable Class="table-hover" Items="records" Context="model">
        <TableHeadTemplate>
            <tr>
                <th>Date</th>
                <th>Amount</th>
                <th>Description</th>
                <th>Category</th>
            </tr>
        </TableHeadTemplate>
        <TableRowTemplate>
            <tr>
                <td>@model.Date.ToLocalTime().ToString("dd-MMM-yyyy")</td>
                <td>@model.Amount $</td>
                <td>@model.Description</td>
                <td>@model.Category</td>
            </tr>
        </TableRowTemplate>
        <TableNoItemTemplate>
            <tr>
                <td colspan="4">No records</td>
            </tr>
        </TableNoItemTemplate>
    </BlazorTable>


#### More examples will be coming soon
