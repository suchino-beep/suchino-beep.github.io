   <!DOCTYPE html>
   <html lang="ja">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Salesforce Live Agent Chat</title>
   </head>
   <body>
       <h1>Salesforce Live Agent Chat</h1>
<style type='text/css'>
	.embeddedServiceHelpButton .helpButton .uiButton {
		background-color: #005290;
		font-family: "Arial", sans-serif;
	}
	.embeddedServiceHelpButton .helpButton .uiButton:focus {
		outline: 1px solid #005290;
	}
</style>

<script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
<script type='text/javascript'>
	var initESW = function(gslbBaseURL) {
		embedded_svc.settings.displayHelpButton = true; //または false
		embedded_svc.settings.language = ''; //たとえば、「en」または「en-US」を入力します

		//embedded_svc.settings.defaultMinimizedText = '...'; //(エキスパートとチャットにデフォルト設定)
		//embedded_svc.settings.disabledMinimizedText = '...'; //(エージェントがオフラインにデフォルト設定)

		//embedded_svc.settings.loadingText = ''; //(読み込み中にデフォルト設定)
		//embedded_svc.settings.storageDomain = 'yourdomain.com'; //(リリースのドメインを設定して、訪問者がチャットセッション中にサブドメインを移動できるようにします)

		// チャット の設定
		//embedded_svc.settings.directToButtonRouting = function(prechatFormData) {
			// Dynamically changes the button ID based on what the visitor enters in the pre-chat form.
			// Returns a valid button ID.
		//};
		//embedded_svc.settings.prepopulatedPrechatFields = {}; //事前チャットフォームの項目の自動入力を設定
		//embedded_svc.settings.fallbackRouting = []; //ボタン ID、ユーザー ID、または userId_buttonId の配列
		//embedded_svc.settings.offlineSupportMinimizedText = '...'; //(デフォルトは [お問い合わせ])

		embedded_svc.settings.enabledFeatures = ['LiveAgent'];
		embedded_svc.settings.entryFeature = 'LiveAgent';

		embedded_svc.init(
			'https://suchino-241029connect2-demo.my.salesforce.com',
			'https://suchino-241029connect2-demo.my.site.com/consumer',
			gslbBaseURL,
			'00DIT000003naAH',
			'SDO_Service_Standard_Chat',
			{
				baseLiveAgentContentURL: 'https://c.la1-c2-it3.salesforceliveagent.com/content',
				deploymentId: '572IT000000TWcc',
				buttonId: '573IT000000TWJL',
				baseLiveAgentURL: 'https://d.la1-c2-it3.salesforceliveagent.com/chat',
				eswLiveAgentDevName: 'EmbeddedServiceLiveAgent_Parent04I1N000000000QUAQ_161f7756989',
				isOfflineSupportEnabled: false
			}
		);
	};

	if (!window.embedded_svc) {
		var s = document.createElement('script');
		s.setAttribute('src', 'https://suchino-241029connect2-demo.my.salesforce.com/embeddedservice/5.0/esw.min.js');
		s.onload = function() {
			initESW(null);
		};
		document.body.appendChild(s);
	} else {
		initESW('https://service.force.com');
	}
</script>
       <script type='text/javascript' src='https://c.la1-c2-it3.salesforceliveagent.com/content/g/js/62.0/deployment.js'></script>
       <script type='text/javascript'>
           liveagent.init('https://d.la1-c2-it3.salesforceliveagent.com/chat', '572IT000000TWcc', '00DIT000003naAH');
       </script>
   </body>
   </html>