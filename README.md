# How to perform swiping smoothly when using DataGridTemplateColumn ?
In this article, we will show you how to perform swiping smoothly when using DataGridTemplateColumn in [.NET MAUI DataGrid](https://www.syncfusion.com/maui-controls/maui-datagrid).

## xaml
The code below demonstrates how to perform swiping smoothly when using DataGridTemplateColumn.
```
<ContentPage.BindingContext>
    <local:EmployeeViewModel x:Name="viewModel" />
</ContentPage.BindingContext>

<syncfusion:SfDataGrid x:Name="dataGrid"
                       ItemsSource="{Binding Employees}"
                       ColumnWidthMode="Auto"
                       AutoGenerateColumnsMode="None"
                       AllowSwiping="True"
                       GridLinesVisibility="Both"
                       MaxSwipeOffset="150"
                       RowHeight="60"
                       HeaderGridLinesVisibility="Both">

    <syncfusion:SfDataGrid.LeftSwipeTemplate>
        <DataTemplate>
            <Grid BackgroundColor="#6750A4"
                  Padding="0">
                <Label Text="EDIT"
                       HorizontalTextAlignment="Center"
                       TextColor="#FFFFFF"
                       VerticalTextAlignment="Center"
                       LineBreakMode="NoWrap"
                       BackgroundColor="Transparent" />
            </Grid>
        </DataTemplate>
    </syncfusion:SfDataGrid.LeftSwipeTemplate>

    <syncfusion:SfDataGrid.Columns>
        <syncfusion:DataGridNumericColumn MappingName="EmployeeID"
                                          Format="#"
                                          HeaderText="Employee ID" />
        <syncfusion:DataGridTemplateColumn MappingName="Name"
                                           HeaderText="Employee Details">
            <syncfusion:DataGridTemplateColumn.CellTemplate>
                <DataTemplate>
                    <Grid InputTransparent="True"
                          ColumnSpacing="0"
                          RowSpacing="0"
                          HorizontalOptions="FillAndExpand"
                          Margin="0"
                          ColumnDefinitions="*,*,*"
                          RowDefinitions="10,*,10">
                        <StackLayout Margin="2"
                                     BackgroundColor="White"
                                     Orientation="Vertical"
                                     HorizontalOptions="FillAndExpand"
                                     VerticalOptions="FillAndExpand"
                                     Grid.Column="0"
                                     Grid.ColumnSpan="3"
                                     Grid.Row="1">
                            <StackLayout Orientation="Horizontal"
                                         HorizontalOptions="FillAndExpand">
                                <Label Text="Employee ID: "
                                       HorizontalTextAlignment="Start"
                                       FontSize="13"
                                       Padding="0,0,4,0" />
                                <Label Text="{Binding EmployeeID}"
                                       FontAttributes="Bold"
                                       TextColor="Black"
                                       FontSize="13"
                                       HorizontalTextAlignment="Start" />
                            </StackLayout>
                            <StackLayout Orientation="Horizontal"
                                         HorizontalOptions="FillAndExpand">
                                <Label Text="Employee Name:"
                                       HorizontalTextAlignment="Start"
                                       FontSize="13"
                                       Padding="0,0,4,0" />
                                <Label Text="{Binding Name}"
                                       FontAttributes="Bold"
                                       TextColor="Black"
                                       FontSize="13"
                                       HorizontalTextAlignment="Start" />
                            </StackLayout>
                        </StackLayout>
                    </Grid>
                </DataTemplate>
            </syncfusion:DataGridTemplateColumn.CellTemplate>
        </syncfusion:DataGridTemplateColumn>
        <syncfusion:DataGridTextColumn MappingName="Title"
                                       HeaderText="Designation" />
        <syncfusion:DataGridDateColumn MappingName="HireDate"
                                       HeaderText="Hire Date" />

    </syncfusion:SfDataGrid.Columns>
</syncfusion:SfDataGrid>
``` 

<img src="https://support.syncfusion.com/kb/agent/attachment/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjM1MDQwIiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.4d3u3V5hbVwUNr2AHrX76Ml_tx5i4hp40EctJ4XQhgE" width=700 />

[View sample in GitHub](https://github.com/SyncfusionExamples/How-to-perform-swiping-on-a-DataGridTemplateColumn)

Take a moment to explore this [documentation](https://help.syncfusion.com/maui/datagrid/overview), where you can find more information about Syncfusion .NET MAUI DataGrid (SfDataGrid) with code examples. Please refer to this [link](https://www.syncfusion.com/maui-controls/maui-datagrid) to learn about the essential features of Syncfusion .NET MAUI DataGrid (SfDataGrid).
 
##### Conclusion
 
I hope you enjoyed learning about how to perform swiping smoothly when using DataGridTemplateColumn in the .NET MAUI DataGrid (SfDataGrid).
 
You can refer to our [.NET MAUI DataGrid’s feature tour](https://www.syncfusion.com/maui-controls/maui-datagrid) page to learn about its other groundbreaking feature representations. You can also explore our [.NET MAUI DataGrid Documentation](https://help.syncfusion.com/maui/datagrid/getting-started) to understand how to present and manipulate data. 
For current customers, you can check out our .NET MAUI components on the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/maui) to explore our .NET MAUI DataGrid and other .NET MAUI components.
 
If you have any queries or require clarifications, please let us know in the comments below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/create) or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sfdatagrid), or the feedback portal. We are always happy to assist you!