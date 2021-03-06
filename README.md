ViewToPDF
=========

iOS Component which generates PDF file from a view.

# Supported UI components
- UIView with background color and subviews
- UILabel with text and background colors
- UIImageView with image or background color

# Instalation
1. Add CoreText framework to the project.
2. Add ViewToPDF.m and ViewToPDF.h files to the project.
3. Include (#import) ViewToPDF.h file to the ViewController from which you would like to render PDF file.

# Properties
1. NSString *fullPDFPath - full path to the rendered PDF file

# Methods
1. initWithView:(UIView*)view andPDFFileName:(NSString*)PDFFileName
parameters:
1.1 view - UIView to render PDF from
1.2 PDFFileName - name of the PDF file

2. render - render PDF file from specified view

# Example
	// Create and instance of viewToPDF
	ViewToPDF *viewToPDF = [[ViewToPDF alloc] initWithView:self.reportView andPDFFileName:@"my_pdg.pdf"];
	// Render method renders PDF file from the reportView view
    [viewToPDF render];
    // This property showf the full path to rendered PDF file
    NSLog(@"PDF File path: %@",viewToPDF.fullPDFPath);