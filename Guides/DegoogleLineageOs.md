# Remove Google-dependencies
As Android / LineageOS is a google software, there are some sintinels deeply baked in the system. We will remove them.

## 1. DNS

Not every servername should be resolved by google:

1. Navigate to Settings - Network and Internet - Advanced - Private DNS
2. Enter new DNS: `dns3.digitalcourage.de`

## 2. Google captive Portal

The question whether you are connected to the internet should not be googles decission:

1. Replace Google captive portal check with [Kuketz](https://www.kuketz-blog.de/android-captive-portal-check-204-http-antwort-von-captiveportal-kuketz-de/). Therefore, connect your Fairphone with your computer and execute following adb commands:  
   ```
   adb shell 'settings put global captive_portal_http_url "http://captiveportal.kuketz.de"'
   adb shell 'settings put global captive_portal_https_url "https://captiveportal.kuketz.de"'
   adb shell 'settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"'
   adb shell 'settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"'
   ```

In order to test the settings, if they were correctly adopted, you can type in:
`adb shell 'settings get global captive_portal_https_url'`

## 3. Google print service

Did you ever use the google print-service? If not, let's switch it off:

1. Switch off Print Service (Settings - Connected devices - Connection preferences - Printing).

## 4. Phone number lookup

LineageOS looks online for the entered number, but that is not their business.

1. Switch of the forward lookup, the people lookup and the reverse lookup (Telephone-App - three points in the search field - Settings - phone number lookup).

## 6. Alternative Browser

Do not trust Googles Browser
1. Open Fdroid to install a Browser. We use Fennec ...
2. Open Fennec and install "privacy badger" & mBlockOrigin as add-on.
3. Drag your Fennec-App-Symbol to the Browserlocation (at the bottom of your screen) & remove chromium

## 7. Location Tracking

Nobody should track your location:

1. Check Privacy Settings and GPS (especially browser-settings from Fennec).


## 8. Browser search suggestions

Not every input on your keyboard has to be sent to the search engine, especially not to Google.

1. Choose another search engine e.g. startpage or duckduckgo (Browser - Settings - Search)
1. Switch off the search suggestions (Browser - Settings - Search - Show search suggestions)


## 9. Deny net access for untrusted apps

If you have to use less trustworthy apps, a firewall is very usefull. We use NetGuard ...
1. FDroid -> search for NetGuard -> install.
