# VLC plugin extension

To package independent plugins for VLC you can create an extension org.videolan.VLC.Plugin.myplugin.

The files in your extension will be available in /app/share/vlc/extra/myplugin.

The lib folder will automatically be added in the runtime LD search paths so you can link your plugin to whatever is there.

To add a VLC plugin put the .so inside a plugins directory at the root of your extension. It will then be available to VLC.

All the .sh files available at the root of the extension will be sourced before launching VLC. You can then mess around with environment variables, and also modify VLC_ARGS which will be prepend to the args passed by the user.

            - 名稱：設定Go環境
  使用：actions/setup-go@v5.0.0
  和：
    # 要下載（如果需要）和使用的 Go 版本。支援 semver 規範和範圍。請務必將此選項用單引號引起來。
    go-version: # 可選
    # go.mod 或 go.work 檔案的路徑。
    go-version-file: # 可選
    # 如果您希望操作始終檢查符合版本規範的最新可用版本，請將此選項設為 true
    檢查最新: # 可選
    # 用於從 go-versions 擷取 Go 發行版。由於存在預設值，因此使用者通常不會提供該預設值。在 github.com 上執行此操作時，預設值就足夠了。在 GHES 上運行時，如果遇到速率限制，您可以傳遞 github.com 的個人存取權杖。
    token: # 可選，預設為 ${{ github.server_url == 'https://github.com' && github.token || '' }}
    # 用於指定是否需要快取。如果您想啟用緩存，請設定為 true。
    快取：# 可選，預設為 true
    # 用於指定依賴檔案的路徑 - go.sum
    快取依賴路徑: # 可選
    # Go 使用的目標架構。範例：x86、x64。預設使用系統架構。
    架構：# 可選
          
