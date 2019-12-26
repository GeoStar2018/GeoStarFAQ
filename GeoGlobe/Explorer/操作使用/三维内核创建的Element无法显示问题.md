问题描述：

三维内核创建的Element无法显示问题


问题解答：

需要将Element添加至图层中。

> 
> if (!m_ptrCurrentLayer)
> {
> 	m_ptrCurrentLayer = new Gs3DElementLayer();
> 	m_ptrCurrentLayer->Name("SituationSymbolLayer");
> 	QgsSceneContextPtr ptrViewContext = viewContext().dynamicCast<QgsSceneContext>();
> 	ptrViewContext->sceneGraph()->LayerContainer()->AddLayer(m_ptrCurrentLayer);
> }
> 
> GsPointElementPtr ptrEle = new GsPointElement(pEle->Geometry(), m_ptrSymbol, true); //GsPointElement为GsGeoElement派生类
> m_ptrCurrentLayer->AddElement(ptrEle);
