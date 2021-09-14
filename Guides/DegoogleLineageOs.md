# Remove Google-dependencies
As Android / LineageOS is a google software, there are some sintinels deeply baked in the system. We will remove them.

## 1. DNS
Not every servername should be resolved by google:

1. enter new DNS: dns2.digitalcourage.de (Settings - Network and Internet - Advanced - Private DNS).

## 2. Location Tracking
Nobody should track your location:

1. Check Privacy Settings and GPS (especially browser-settings from Fennec).

## 3. google print service
Did you ever use the google print-service? If not, let's switch it off:

1. Switch off Print Service (Settings - Connected devices - Connection preferences - Printing).

## 4. Google captive Portal
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
