
Von Anthony, Davud, Sebastian, Maximilian, Tyrone & Nesim

# Xamarin.Forms und .NET MAUI Übersicht

## Inhaltsverzeichnis


  - [Inhaltsverzeichnis](#inhaltsverzeichnis)
  - [1. Layouts und Navigationen:](#1-layouts-und-navigationen)
    - [1.1 Layouts:](#11-layouts)
    - [1.2 Navigationen:](#12-navigationen)
  - [2. Layout-Manager:](#2-layout-manager)
  - [3. Gängige Steuerelemente (Code Beispiele):](#3-gängige-steuerelemente-code-beispiele)
  - [4. Multi-Device-Unterstützung:](#4-multi-device-unterstützung)


## 1. Layouts und Navigationen:

### 1.1 Layouts:
1. **StackLayout**: Stapelt Elemente vertikal oder horizontal.
   ```xml
   <StackLayout>
       <!-- Elemente hier -->
   </StackLayout>
   ```

2. **Grid**: Ordnet Elemente in Zeilen und Spalten an.
   ```xml
   <Grid>
       <!-- Elemente hier -->
   </Grid>
   ```

3. **AbsoluteLayout**: Positioniert Elemente an absoluten Koordinaten.
   ```xml
   <AbsoluteLayout>
       <!-- Elemente hier -->
   </AbsoluteLayout>
   ```

### 1.2 Navigationen:
1. **NavigationPage**: Verwaltet einen Stapel von Seiten mit Navigation.
   ```csharp
   await Navigation.PushAsync(new PageName());
   await Navigation.PopAsync();
   ```

2. **TabbedPage**: Stellt Registerkarten dar.
   ```xml
   <TabbedPage>
       <TabbedPage.Children>
           <!-- Seiten hier -->
       </TabbedPage.Children>
   </TabbedPage>
   ```

3. **MasterDetailPage**: Ermöglicht eine Master-Detail-Navigation.
   ```xml
   <MasterDetailPage>
       <MasterDetailPage.Master>
           <!-- Master Seite -->
       </MasterDetailPage.Master>
       <MasterDetailPage.Detail>
           <!-- Detail Seite -->
       </MasterDetailPage.Detail>
   </MasterDetailPage>
   ```

## 2. Layout-Manager:
Xamarin.Forms und .NET MAUI verwenden einen nativen Layout-Manager für jede Plattform, der die UI-Elemente entsprechend der XAML-Beschreibungen positioniert.

## 3. Gängige Steuerelemente (Code Beispiele):
1. **Button**:
   ```xml
   <Button Text="Click Me" Clicked="Handle_Clicked" />
   ```

2. **Entry**:
   ```xml
   <Entry Placeholder="Enter text" />
   ```

3. **Label**:
   ```xml
   <Label Text="Hello, World!" />
   ```

4. **ListView**:
   ```xml
   <ListView ItemsSource="{Binding Items}">
       <ListView.ItemTemplate>
           <DataTemplate>
               <TextCell Text="{Binding}" />
           </DataTemplate>
       </ListView.ItemTemplate>
   </ListView>
   ```

## 4. Multi-Device-Unterstützung:
Xamarin.Forms und .NET MAUI ermöglichen die Entwicklung von plattformübergreifenden Anwendungen, die auf verschiedenen Geräten wie Mobiltelefonen, Tablets und Desktops ausgeführt werden können. Dabei werden die nativen Steuerelemente und Layouts der jeweiligen Plattformen verwendet, um eine native Benutzererfahrung zu bieten. Durch responsive Layouts und adaptive UIs können Apps an verschiedene Bildschirmgrößen und -auflösungen angepasst werden. Zudem bieten sie Funktionen wie Dependency Injection und Plattform-abhängige Implementierungen für eine gerätespezifische Anpassung.
