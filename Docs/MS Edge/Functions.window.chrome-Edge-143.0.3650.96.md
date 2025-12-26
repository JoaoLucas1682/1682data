Pra quem quiser explorar mais porque não tô com tempo agora,
Executei a seguinte função:
```
function listFunctions(obj, prefix = "") {
  Object.keys(obj).forEach(key => {
    try {
      if (typeof obj[key] === "function") {
        console.log(`Função encontrada: ${prefix}${key}`);
      } else if (typeof obj[key] === "object" && obj[key] !== null) {
        listFunctions(obj[key], `${prefix}${key}.`);
      }
    } catch (e) {
      console.warn(`Não podê acessar ${prefix}${key}:`, e);
    }
  });
}

listFunctions(window.chrome);
```
e de repente descobri as funções do window.chrome no Edge (143.0.3650.96):

```
VM1565:5 Função encontrada: loadTimes
00:53:10.443 VM1565:5 Função encontrada: csi
00:53:10.443 VM1565:5 Função encontrada: app.getDetails
00:53:10.443 VM1565:5 Função encontrada: app.getIsInstalled
00:53:10.443 VM1565:5 Função encontrada: app.installState
00:53:10.443 VM1565:5 Função encontrada: app.runningState
00:53:10.444 VM1565:5 Função encontrada: copilotLabPrivate.enableCopilotLab
00:53:10.444 VM1565:5 Função encontrada: copilotLabPrivate.enableEdgeTools
00:53:10.444 VM1565:5 Função encontrada: copilotLabPrivate.enableJourneys
00:53:10.444 VM1565:5 Função encontrada: copilotLabPrivate.getCopilotLabState
00:53:10.444 VM1565:5 Função encontrada: copilotLabPrivate.getEdgeToolsState
00:53:10.444 VM1565:5 Função encontrada: copilotLabPrivate.getJourneysState
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.activateContinuousImport
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.activateTriggerWithPageType
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.enableCIForRewardsSweepstakes
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.getAppInfo
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.getClientInfo
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.hasSyncedOnMobile
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.installTheme
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.isAIGenThemesPolicyEnabled
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.isEdgeChatAutoOpenEnabled
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.isEdgeChatEnabled
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.isEdgeChatVisible
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.openHub
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.openSettingsUrl
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.openSplitScreen
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.openUrl
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.openWorkspaces
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.performAction
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.performActionWithParams
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.pinSite
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.pinSiteForRewardsSweepstakes
00:53:10.444 VM1565:5 Função encontrada: edgeMarketingPagePrivate.sendCopilotQuery
00:53:10.445 VM1565:5 Função encontrada: edgeMarketingPagePrivate.setImageAsBrowserTheme
00:53:10.445 VM1565:5 Função encontrada: edgeMarketingPagePrivate.setImageAsBrowserThemeForRewardsSweepstakes
00:53:10.445 VM1565:5 Função encontrada: edgeMarketingPagePrivate.setPref
00:53:10.445 VM1565:5 Função encontrada: edgeMarketingPagePrivate.setTabStripHorizontal
00:53:10.445 VM1565:5 Função encontrada: edgeMarketingPagePrivate.setTabStripVertical
00:53:10.445 VM1565:5 Função encontrada: edgeCopilotPrivate.isVisionEnabledForUser
00:53:10.445 VM1565:5 Função encontrada: edgeCopilotPrivate.launchVision
00:53:10.445 VM1565:5 Função encontrada: edgeCopilotPrivate.navigateToCopilotPage
00:53:10.445 VM1565:5 Função encontrada: runtime.connect
00:53:10.445 VM1565:5 Função encontrada: runtime.sendMessage
```

Caso alguém quiser explorar tá aí.

Edit 1: Isto só funciona em páginas específicas. Em uma página comum (tipo o about:blank), a(s) função(ões) não aparece.

