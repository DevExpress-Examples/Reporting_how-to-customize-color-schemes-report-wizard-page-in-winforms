# How to customize the Choose a Report Color Scheme wizard page in WinForms
This example demonstrates how to customize the [Choose a Report Color Scheme](https://docs.devexpress.com/XtraReports/400389/visual-studio-report-designer/report-wizard/table-report/choose-a-report-color-scheme) wizard page in WinForms applications.

Below are the main steps to change the color scheme set on the Report Wizard page:

1. Implement the <a href="https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.Wizards.ColorSchemes.IColorSchemeStorage">IColorSchemeStorage</a> interface to create a storage for the wizard's custom color schemes.
2. Use the <a href="https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.Wizards.ColorSchemes.IColorSchemeStorage.AddColorScheme(DevExpress.XtraReports.Wizards.ColorSchemes.ColorScheme)">AddColorScheme</a> method to add custom color schemes to the created storage.
3. Add a custom service that implements the <a href="https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.Wizards.IWizardCustomizationService">IWizardCustomizationService</a> interface. 
4. Register the custom color scheme storage in the <a href="https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.Wizards.IWizardCustomizationService.CustomizeReportWizard(IWizardCustomization-XtraReportModel-)">CustomizeReportWizard</a> method.
5. Call the <a href="https://docs.devexpress.com/XtraReports/DevExpress.XtraReports.UserDesigner.XRDesignMdiController.AddService.method(h6ad2Q) ">XRDesignMdiController.AddService</a> method to register the created service.
