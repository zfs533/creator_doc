```
├── AUTHORS.txt
├── CHANGELOG.txt
├── DebugInfos.json
├── EngineErrorMap.md
├── MAINTAINERS
├── README.md
├── api.d.ts
├── bin
│   ├── cocos2d-js-for-preview.js
│   ├── cocos2d-js-for-preview.js.map
│   ├── cocos2d-jsb-for-preview.js
│   ├── cocos2d-jsb-min.js
│   └── cocos2d-jsb.js
├── cocos2d
│   ├── actions
│   │   ├── CCAction.js    动作基类
│   │   ├── CCActionCatmullRom.js  曲线轨迹运动API
│   │   ├── CCActionEase.js     缓动动作API
│   │   ├── CCActionInstant.js  即时动作API
│   │   ├── CCActionInterval.js  时间间隔动作API
│   │   ├── CCActionManager.js  动作管理API，给节点单独添加动作，获取节点所有动作
│   │   ├── index.js    入口
│   │   └── tween.js    tween动作API
│   ├── animation
│   │   ├── animation-animator.js  动画基类API
│   │   ├── animation-clip.js 动画剪辑API
│   │   ├── animation-curves.js 动画曲线API
│   │   ├── animation-manager.js 动画管理API
│   │   ├── animation-state.js 动画状态监听API
│   │   ├── bezier.js  贝塞尔曲线算法
│   │   ├── easing.js 缓动动画API
│   │   ├── index.js 入口
│   │   ├── motion-path-helper.js  动作曲线帮助
│   │   ├── playable.js
│   │   └── types.js  类型枚举API
│   ├── audio
│   │   ├── CCAudio.js  音效基类
│   │   └── CCAudioEngine.js 音效引擎API
│   ├── compression  压缩工具
│   │   ├── ZipUtils.js 
│   │   ├── base64.js base64加密解密API
│   │   ├── gzip.js
│   │   └── zlib.min.js
│   ├── core
│   │   ├── 3d
│   │   │   ├── CCLightComponent.js
│   │   │   ├── CCModel.js
│   │   │   ├── actions.js
│   │   │   ├── index.js
│   │   │   ├── particle
│   │   │   │   ├── animator
│   │   │   │   │   ├── color-overtime.ts
│   │   │   │   │   ├── curve-range.ts
│   │   │   │   │   ├── force-overtime.ts
│   │   │   │   │   ├── gradient-range.ts
│   │   │   │   │   ├── gradient.ts
│   │   │   │   │   ├── limit-velocity-overtime.ts
│   │   │   │   │   ├── optimized-curve.ts
│   │   │   │   │   ├── rotation-overtime.ts
│   │   │   │   │   ├── size-overtime.ts
│   │   │   │   │   ├── texture-animation.ts
│   │   │   │   │   └── velocity-overtime.ts
│   │   │   │   ├── burst.ts
│   │   │   │   ├── curve.ts
│   │   │   │   ├── emitter
│   │   │   │   │   └── shape-module.ts
│   │   │   │   ├── enum.ts
│   │   │   │   ├── particle-general-function.ts
│   │   │   │   ├── particle-system-3d.ts
│   │   │   │   ├── particle-utils.ts
│   │   │   │   ├── particle.ts
│   │   │   │   ├── renderer
│   │   │   │   │   ├── particle-batch-model.ts
│   │   │   │   │   ├── particle-system-3d-renderer.ts
│   │   │   │   │   └── trail.ts
│   │   │   │   └── utils.ts
│   │   │   ├── physics
│   │   │   │   ├── cannon
│   │   │   │   │   ├── cannon-rigid-body.ts
│   │   │   │   │   ├── cannon-shared-body.ts
│   │   │   │   │   ├── cannon-util.ts
│   │   │   │   │   ├── cannon-world.ts
│   │   │   │   │   ├── instantiate.ts
│   │   │   │   │   └── shapes
│   │   │   │   │       ├── cannon-box-shape.ts
│   │   │   │   │       ├── cannon-shape.ts
│   │   │   │   │       └── cannon-sphere-shape.ts
│   │   │   │   ├── cocos
│   │   │   │   │   ├── builtin-interface.ts
│   │   │   │   │   ├── builtin-shared-body.ts
│   │   │   │   │   ├── builtin-world.ts
│   │   │   │   │   ├── instantiate.ts
│   │   │   │   │   ├── shapes
│   │   │   │   │   │   ├── builtin-box-shape.ts
│   │   │   │   │   │   ├── builtin-shape.ts
│   │   │   │   │   │   └── builtin-sphere-shape.ts
│   │   │   │   │   └── utils
│   │   │   │   │       └── array-collision-matrix.ts
│   │   │   │   ├── exports
│   │   │   │   │   ├── physics-builtin.ts
│   │   │   │   │   ├── physics-cannon.ts
│   │   │   │   │   └── physics-framework.ts
│   │   │   │   ├── framework
│   │   │   │   │   ├── assets
│   │   │   │   │   │   └── physics-material.ts
│   │   │   │   │   ├── components
│   │   │   │   │   │   ├── collider
│   │   │   │   │   │   │   ├── box-collider-component.ts
│   │   │   │   │   │   │   ├── collider-component.ts
│   │   │   │   │   │   │   └── sphere-collider-component.ts
│   │   │   │   │   │   ├── constant-force.ts
│   │   │   │   │   │   └── rigid-body-component.ts
│   │   │   │   │   ├── index.ts
│   │   │   │   │   ├── instance.ts
│   │   │   │   │   ├── physics-enum.ts
│   │   │   │   │   ├── physics-interface.ts
│   │   │   │   │   ├── physics-manager.ts
│   │   │   │   │   ├── physics-ray-result.ts
│   │   │   │   │   ├── physics-selector.ts
│   │   │   │   │   └── util.ts
│   │   │   │   └── spec
│   │   │   │       ├── I-rigid-body.ts
│   │   │   │       ├── i-common.ts
│   │   │   │       ├── i-physics-shape.ts
│   │   │   │       └── i-physics-world.ts
│   │   │   ├── primitive
│   │   │   │   ├── box.ts
│   │   │   │   ├── capsule.ts
│   │   │   │   ├── cone.ts
│   │   │   │   ├── cylinder.ts
│   │   │   │   ├── index.ts
│   │   │   │   ├── plane.ts
│   │   │   │   ├── polyhedron.ts
│   │   │   │   ├── quad.ts
│   │   │   │   ├── sphere.ts
│   │   │   │   ├── torus.ts
│   │   │   │   ├── utils.ts
│   │   │   │   └── vertex-data.ts
│   │   │   └── skeleton
│   │   │       ├── CCJointMatrixCurve.js
│   │   │       ├── CCSkeleton.js
│   │   │       ├── CCSkeletonAnimation.js
│   │   │       ├── CCSkeletonAnimationClip.js
│   │   │       ├── CCSkinnedMeshRenderer.js
│   │   │       └── skinned-mesh-renderer.js
│   │   ├── CCDebug.js
│   │   ├── CCDirector.js 导演类API
│   │   ├── CCGame.js   游戏监听API 进入后台，暂停，重启，退出游戏1
│   │   ├── CCNode.js   Node API
│   │   ├── CCPrivateNode.js 场景中的私有节点类  * 私有节点在编辑器中不可见，对用户透明
│   │   ├── CCScene.js
│   │   ├── CCScheduler.js
│   │   ├── asset-manager
│   │   │   ├── CCAssetManager.js
│   │   │   ├── builtins.js
│   │   │   ├── bundle.js
│   │   │   ├── cache-manager.d.ts
│   │   │   ├── cache.js
│   │   │   ├── config.js
│   │   │   ├── depend-util.js
│   │   │   ├── deprecated.js
│   │   │   ├── deserialize.js
│   │   │   ├── download-dom-audio.js
│   │   │   ├── download-dom-image.js
│   │   │   ├── download-file.js
│   │   │   ├── download-script.js
│   │   │   ├── downloader.js
│   │   │   ├── factory.js
│   │   │   ├── fetch.js
│   │   │   ├── font-loader.js
│   │   │   ├── helper.js
│   │   │   ├── index.js
│   │   │   ├── load.js
│   │   │   ├── pack-manager.js
│   │   │   ├── parser.js
│   │   │   ├── pipeline.js
│   │   │   ├── preprocess.js
│   │   │   ├── releaseManager.js
│   │   │   ├── request-item.js
│   │   │   ├── shared.js
│   │   │   ├── task.js
│   │   │   ├── urlTransformer.js
│   │   │   └── utilities.js
│   │   ├── assets
│   │   │   ├── CCAsset.js
│   │   │   ├── CCAudioClip.js
│   │   │   ├── CCBitmapFont.js
│   │   │   ├── CCBufferAsset.js
│   │   │   ├── CCFont.js
│   │   │   ├── CCJsonAsset.js
│   │   │   ├── CCLabelAtlas.js
│   │   │   ├── CCPrefab.js
│   │   │   ├── CCRenderTexture.js
│   │   │   ├── CCSceneAsset.js
│   │   │   ├── CCScripts.js
│   │   │   ├── CCSpriteAtlas.js
│   │   │   ├── CCSpriteFrame.js
│   │   │   ├── CCTTFFont.js
│   │   │   ├── CCTextAsset.js
│   │   │   ├── CCTexture2D.js
│   │   │   ├── index.js
│   │   │   └── material
│   │   │       ├── CCEffectAsset.js
│   │   │       ├── CCMaterial.js
│   │   │       ├── effect-base.ts
│   │   │       ├── effect-parser.ts
│   │   │       ├── effect-variant.ts
│   │   │       ├── effect.ts
│   │   │       ├── index.js
│   │   │       ├── material-pool.js
│   │   │       ├── material-variant.ts
│   │   │       └── utils.js
│   │   ├── base-ui
│   │   │   └── CCWidgetManager.js
│   │   ├── camera
│   │   │   └── CCCamera.js
│   │   ├── collider
│   │   │   ├── CCBoxCollider.js
│   │   │   ├── CCCircleCollider.js
│   │   │   ├── CCCollider.js
│   │   │   ├── CCCollisionManager.js
│   │   │   ├── CCContact.js
│   │   │   ├── CCIntersection.js   矩形碰撞检查，矩形与多边形碰撞检查
│   │   │   ├── CCPolygonCollider.js 多边形碰撞检查
│   │   │   └── index.js
│   │   ├── component-scheduler.js
│   │   ├── components
│   │   │   ├── CCAnimation.js
│   │   │   ├── CCAudioSource.js
│   │   │   ├── CCBlockInputEvents.js
│   │   │   ├── CCButton.js
│   │   │   ├── CCCanvas.js
│   │   │   ├── CCComponent.js
│   │   │   ├── CCComponentEventHandler.js
│   │   │   ├── CCLabel.js
│   │   │   ├── CCLabelOutline.js
│   │   │   ├── CCLabelShadow.js
│   │   │   ├── CCLayout.js
│   │   │   ├── CCMask.js
│   │   │   ├── CCMotionStreak.js
│   │   │   ├── CCPageView.js
│   │   │   ├── CCPageViewIndicator.js
│   │   │   ├── CCProgressBar.js
│   │   │   ├── CCRenderComponent.js
│   │   │   ├── CCRichText.js
│   │   │   ├── CCSafeArea.js
│   │   │   ├── CCScrollBar.js
│   │   │   ├── CCScrollView.js
│   │   │   ├── CCSlider.js
│   │   │   ├── CCSprite.js
│   │   │   ├── CCStudioComponent.js
│   │   │   ├── CCToggle.js
│   │   │   ├── CCToggleContainer.js
│   │   │   ├── CCToggleGroup.js
│   │   │   ├── CCViewGroup.js
│   │   │   ├── CCWidget.js
│   │   │   ├── SwanSubContextView.js
│   │   │   ├── WXSubContextView.js
│   │   │   ├── editbox
│   │   │   │   ├── CCEditBox.js
│   │   │   │   ├── EditBoxImplBase.js
│   │   │   │   ├── WebEditBoxImpl.js
│   │   │   │   ├── tabIndexUtil.js
│   │   │   │   └── types.js
│   │   │   ├── index.js
│   │   │   └── missing-script.js
│   │   ├── event
│   │   │   ├── event-listeners.js
│   │   │   ├── event-target.js
│   │   │   ├── event.js
│   │   │   ├── index.js
│   │   │   └── system-event.js
│   │   ├── event-manager
│   │   │   ├── CCEvent.js
│   │   │   ├── CCEventListener.js
│   │   │   ├── CCEventManager.js
│   │   │   ├── CCTouch.js
│   │   │   └── index.js
│   │   ├── geom-utils
│   │   │   ├── aabb.ts
│   │   │   ├── distance.ts
│   │   │   ├── enums.ts
│   │   │   ├── frustum.ts
│   │   │   ├── index.ts
│   │   │   ├── intersect.ts
│   │   │   ├── line.ts
│   │   │   ├── obb.ts
│   │   │   ├── plane.ts
│   │   │   ├── ray.ts
│   │   │   ├── sphere.ts
│   │   │   └── triangle.ts
│   │   ├── graphics
│   │   │   ├── graphics.js
│   │   │   ├── helper.js
│   │   │   ├── index.js
│   │   │   └── types.js
│   │   ├── index.js
│   │   ├── mesh
│   │   │   ├── CCMesh.js
│   │   │   ├── CCMeshRenderer.js
│   │   │   ├── index.js
│   │   │   ├── mesh-data.js
│   │   │   └── mesh-renderer.js
│   │   ├── node-activator.js
│   │   ├── physics
│   │   │   ├── CCPhysicsContact.js
│   │   │   ├── CCPhysicsManager.js
│   │   │   ├── CCPhysicsTypes.js
│   │   │   ├── CCPolygonSeparator.js
│   │   │   ├── CCRigidBody.js
│   │   │   ├── box2d-adapter.js
│   │   │   ├── collider
│   │   │   │   ├── CCPhysicsBoxCollider.js
│   │   │   │   ├── CCPhysicsChainCollider.js
│   │   │   │   ├── CCPhysicsCircleCollider.js
│   │   │   │   ├── CCPhysicsCollider.js
│   │   │   │   └── CCPhysicsPolygonCollider.js
│   │   │   ├── index.js
│   │   │   ├── joint
│   │   │   │   ├── CCDistanceJoint.js
│   │   │   │   ├── CCJoint.js
│   │   │   │   ├── CCMotorJoint.js
│   │   │   │   ├── CCMouseJoint.js
│   │   │   │   ├── CCPrismaticJoint.js
│   │   │   │   ├── CCRevoluteJoint.js
│   │   │   │   ├── CCRopeJoint.js
│   │   │   │   ├── CCWeldJoint.js
│   │   │   │   └── CCWheelJoint.js
│   │   │   ├── platform
│   │   │   │   ├── CCPhysicsAABBQueryCallback.js
│   │   │   │   ├── CCPhysicsContactListner.js
│   │   │   │   ├── CCPhysicsDebugDraw.js
│   │   │   │   └── CCPhysicsRayCastCallback.js
│   │   │   └── utils.js
│   │   ├── platform
│   │   │   ├── CCClass.js
│   │   │   ├── CCClassDecorator.js
│   │   │   ├── CCEnum.js
│   │   │   ├── CCInputExtension.js
│   │   │   ├── CCInputManager.js
│   │   │   ├── CCMacro.js
│   │   │   ├── CCObject.js
│   │   │   ├── CCSAXParser.js
│   │   │   ├── CCScreen.js
│   │   │   ├── CCSys.js
│   │   │   ├── CCView.js
│   │   │   ├── CCVisibleRect.js
│   │   │   ├── attribute.js
│   │   │   ├── callbacks-invoker.js
│   │   │   ├── compiler.js
│   │   │   ├── deserialize.js
│   │   │   ├── id-generater.js
│   │   │   ├── index.js
│   │   │   ├── instantiate-jit.js
│   │   │   ├── instantiate.js
│   │   │   ├── js.js
│   │   │   ├── preprocess-class.js
│   │   │   ├── requiring-frame.js
│   │   │   └── utils.js
│   │   ├── predefine.js
│   │   ├── renderer
│   │   │   ├── assembler-2d.js
│   │   │   ├── assembler-3d.js
│   │   │   ├── assembler-pool.js
│   │   │   ├── assembler.js
│   │   │   ├── canvas
│   │   │   │   ├── Device.js
│   │   │   │   ├── Texture2D.js
│   │   │   │   ├── forward-renderer.js
│   │   │   │   ├── index.js
│   │   │   │   ├── render-component-handle.js
│   │   │   │   ├── render-flow.js
│   │   │   │   └── renderers
│   │   │   │       ├── graphics
│   │   │   │       │   ├── impl.js
│   │   │   │       │   └── index.js
│   │   │   │       ├── index.js
│   │   │   │       ├── label
│   │   │   │       │   ├── bmfont.js
│   │   │   │       │   ├── index.js
│   │   │   │       │   └── ttf.js
│   │   │   │       ├── mask.js
│   │   │   │       ├── render-data.js
│   │   │   │       ├── sprite
│   │   │   │       │   ├── index.js
│   │   │   │       │   ├── simple.js
│   │   │   │       │   ├── sliced.js
│   │   │   │       │   └── tiled.js
│   │   │   │       └── utils.js
│   │   │   ├── index.js
│   │   │   ├── render-flow.js
│   │   │   ├── utils
│   │   │   │   ├── dynamic-atlas
│   │   │   │   │   ├── atlas.js
│   │   │   │   │   └── manager.js
│   │   │   │   ├── label
│   │   │   │   │   ├── bmfont.js
│   │   │   │   │   ├── label-frame.js
│   │   │   │   │   ├── letter-font.js
│   │   │   │   │   └── ttf.js
│   │   │   │   └── utils.js
│   │   │   └── webgl
│   │   │       ├── assemblers
│   │   │       │   ├── graphics
│   │   │       │   │   ├── earcut.js
│   │   │       │   │   ├── impl.js
│   │   │       │   │   └── index.js
│   │   │       │   ├── index.js
│   │   │       │   ├── label
│   │   │       │   │   ├── 2d
│   │   │       │   │   │   ├── bmfont.js
│   │   │       │   │   │   ├── letter.js
│   │   │       │   │   │   ├── nativeTTF.js
│   │   │       │   │   │   └── ttf.js
│   │   │       │   │   ├── 3d
│   │   │       │   │   │   ├── bmfont.js
│   │   │       │   │   │   ├── letter.js
│   │   │       │   │   │   └── ttf.js
│   │   │       │   │   └── index.js
│   │   │       │   ├── mask-assembler.js
│   │   │       │   ├── motion-streak.js
│   │   │       │   └── sprite
│   │   │       │       ├── 2d
│   │   │       │       │   ├── bar-filled.js
│   │   │       │       │   ├── mesh.js
│   │   │       │       │   ├── radial-filled.js
│   │   │       │       │   ├── simple.js
│   │   │       │       │   ├── sliced.js
│   │   │       │       │   └── tiled.js
│   │   │       │       ├── 3d
│   │   │       │       │   ├── bar-filled.js
│   │   │       │       │   ├── mesh.js
│   │   │       │       │   ├── radial-filled.js
│   │   │       │       │   ├── simple.js
│   │   │       │       │   ├── sliced.js
│   │   │       │       │   └── tiled.js
│   │   │       │       └── index.js
│   │   │       ├── flex-buffer.js
│   │   │       ├── mesh-buffer.js
│   │   │       ├── model-batcher.js
│   │   │       ├── quad-buffer.js
│   │   │       ├── render-data.js
│   │   │       ├── spine-buffer.js
│   │   │       └── vertex-format.js
│   │   ├── utils
│   │   │   ├── CCPath.js
│   │   │   ├── affine-transform.js
│   │   │   ├── base-node.js
│   │   │   ├── binary-search.js
│   │   │   ├── blend-func.js
│   │   │   ├── decode-uuid.js
│   │   │   ├── find.js
│   │   │   ├── gray-sprite-state.js
│   │   │   ├── html-text-parser.js
│   │   │   ├── index.js
│   │   │   ├── math-pools.js
│   │   │   ├── misc.js
│   │   │   ├── mutable-forward-iterator.js
│   │   │   ├── pool.js
│   │   │   ├── prefab-helper.js
│   │   │   ├── profiler
│   │   │   │   ├── CCProfiler.js
│   │   │   │   ├── counter.js
│   │   │   │   └── perf-counter.js
│   │   │   ├── text-utils.js
│   │   │   ├── texture-util.js
│   │   │   └── trans-pool
│   │   │       ├── index.js
│   │   │       ├── mem-pool.js
│   │   │       ├── node-mem-pool.js
│   │   │       ├── node-unit.js
│   │   │       └── unit-base.js
│   │   └── value-types
│   │       ├── color.ts
│   │       ├── index.ts
│   │       ├── mat3.ts
│   │       ├── mat4.ts
│   │       ├── math.d.ts
│   │       ├── quat.ts
│   │       ├── rect.ts
│   │       ├── size.ts
│   │       ├── trs.ts
│   │       ├── utils.ts
│   │       ├── value-type.ts
│   │       ├── vec2.ts
│   │       ├── vec3.ts
│   │       └── vec4.ts
│   ├── deprecated.js
│   ├── index.js
│   ├── particle
│   │   ├── CCPNGReader.js
│   │   ├── CCParticleAsset.js
│   │   ├── CCParticleSystem.js
│   │   ├── CCTIFFReader.js
│   │   ├── index.js
│   │   ├── particle-simulator.js
│   │   └── particle-system-assembler.js
│   ├── renderer
│   │   ├── build
│   │   │   ├── build-mapping.js
│   │   │   ├── chunks
│   │   │   │   ├── alpha-test.inc
│   │   │   │   ├── cc-global.inc
│   │   │   │   ├── cc-lights.inc
│   │   │   │   ├── cc-local.inc
│   │   │   │   ├── common.inc
│   │   │   │   ├── gamma.inc
│   │   │   │   ├── input-standard.inc
│   │   │   │   ├── output.inc
│   │   │   │   ├── packing.inc
│   │   │   │   ├── rect-area-light.inc
│   │   │   │   ├── shader
│   │   │   │   │   ├── particle-common.inc
│   │   │   │   │   ├── particle-trail.inc
│   │   │   │   │   ├── particle-vs-gpu.inc
│   │   │   │   │   ├── particle-vs-legacy.inc
│   │   │   │   │   ├── phong-fs.inc
│   │   │   │   │   ├── phong-vs.inc
│   │   │   │   │   ├── shadow-map-fs.inc
│   │   │   │   │   ├── shadow-map-vs.inc
│   │   │   │   │   ├── unlit-fs.inc
│   │   │   │   │   └── unlit-vs.inc
│   │   │   │   ├── shading-phong.inc
│   │   │   │   ├── shading-toon.inc
│   │   │   │   ├── shadow.inc
│   │   │   │   ├── skinning.inc
│   │   │   │   ├── texture.inc
│   │   │   │   ├── transform.inc
│   │   │   │   └── unpack.inc
│   │   │   └── mappings
│   │   │       ├── gfx
│   │   │       │   └── define.ts
│   │   │       ├── index.js
│   │   │       ├── offline-mappings.ts
│   │   │       └── pipeline
│   │   │           └── define.ts
│   │   ├── core
│   │   │   ├── base-renderer.js
│   │   │   ├── constants.js
│   │   │   ├── input-assembler.js
│   │   │   ├── pass.js
│   │   │   ├── program-lib.js
│   │   │   ├── technique.js
│   │   │   └── view.js
│   │   ├── enums.js
│   │   ├── gfx
│   │   │   ├── device.js
│   │   │   ├── enums.js
│   │   │   ├── frame-buffer.js
│   │   │   ├── index-buffer.js
│   │   │   ├── index.js
│   │   │   ├── misc.js
│   │   │   ├── program.js
│   │   │   ├── render-buffer.js
│   │   │   ├── state.js
│   │   │   ├── texture-2d.js
│   │   │   ├── texture-cube.js
│   │   │   ├── texture.js
│   │   │   ├── vertex-buffer.js
│   │   │   └── vertex-format.js
│   │   ├── memop
│   │   │   ├── circular-pool.js
│   │   │   ├── fixed-array.js
│   │   │   ├── index.js
│   │   │   ├── linked-array.js
│   │   │   ├── optimized-array.js
│   │   │   ├── pool.js
│   │   │   ├── recycle-pool.js
│   │   │   ├── sort.js
│   │   │   ├── timsort.js
│   │   │   └── typed-array-pool.js
│   │   ├── murmurhash2_gc.js
│   │   ├── renderers
│   │   │   └── forward-renderer.js
│   │   ├── scene
│   │   │   ├── camera.js
│   │   │   ├── light.js
│   │   │   ├── model.js
│   │   │   └── scene.js
│   │   └── types.js
│   ├── tilemap
│   │   ├── CCTMXXMLParser.js
│   │   ├── CCTiledLayer.js
│   │   ├── CCTiledMap.js
│   │   ├── CCTiledMapAsset.js
│   │   ├── CCTiledMapRenderDataList.js
│   │   ├── CCTiledObjectGroup.js
│   │   ├── CCTiledTile.js
│   │   ├── editor
│   │   │   ├── tiled-map.html
│   │   │   ├── tiled-map.js
│   │   │   └── tiled-map.png
│   │   ├── index.js
│   │   ├── tiledmap-buffer.js
│   │   └── tmx-layer-assembler.js
│   ├── videoplayer
│   │   ├── CCVideoPlayer.js
│   │   └── video-player-impl.js
│   └── webview
│       ├── CCWebView.js
│       └── webview-impl.js
├── docs
│   ├── apisrc.json
│   ├── cocos2d
│   │   └── core
│   │       ├── CCActionManager
│   │       │   └── ActionManager.js
│   │       ├── CCScheduler
│   │       │   ├── schedule.js
│   │       │   ├── scheduleCallbackForTarget.js
│   │       │   ├── scheduleUpdateForTarget.js
│   │       │   ├── unscheduleCallbackForTarget.js
│   │       │   └── unscheduleUpdateForTarget.js
│   │       ├── animation-clip
│   │       │   ├── curve-data.js
│   │       │   └── event-data.js
│   │       ├── components
│   │       │   └── CCSpriteRenerer
│   │       │       └── initWithSpriteFrameName.js
│   │       ├── event
│   │       │   └── _getCapturingTargets.js
│   │       ├── event-manager
│   │       │   ├── CCEventListener
│   │       │   │   └── create.js
│   │       │   └── CCEventManager
│   │       │       ├── addListener.js
│   │       │       └── removeListener.js
│   │       ├── platform
│   │       │   ├── CCCommon
│   │       │   │   └── KEY.js
│   │       │   ├── CCEnum
│   │       │   │   └── Enum.js
│   │       │   ├── CCMacro
│   │       │   │   └── lerp.js
│   │       │   └── attribute
│   │       │       └── attr.js
│   │       ├── sprites
│   │       │   ├── addSpriteFrames.js
│   │       │   └── getSpriteFrame.js
│   │       ├── textures
│   │       │   ├── TextureAtlas.js
│   │       │   ├── addImage.js
│   │       │   ├── getKeyByTexture.js
│   │       │   ├── getTextureColors.js
│   │       │   ├── getTextureForKey.js
│   │       │   ├── initWithFile.js
│   │       │   ├── initWithTexture.js
│   │       │   ├── removeAllTextures.js
│   │       │   ├── removeTexture.js
│   │       │   ├── removeTextureForKey.js
│   │       │   └── textureForKey.js
│   │       ├── utils
│   │       │   ├── CCPath
│   │       │   │   ├── basename.js
│   │       │   │   ├── changeBasename.js
│   │       │   │   ├── changeExtname.js
│   │       │   │   ├── dirname.js
│   │       │   │   ├── extname.js
│   │       │   │   └── join.js
│   │       │   ├── base-node
│   │       │   │   └── setPosition.js
│   │       │   └── node-wrapper
│   │       │       └── setPosition.js
│   │       └── value-types
│   │           ├── CCColor
│   │           │   ├── color.js
│   │           │   └── lerp.js
│   │           └── CCSize
│   │               └── size.js
│   └── extensions
│       └── ccpool
│           └── putInPool.js
├── editor
│   ├── dashboard
│   │   ├── banner.jpg
│   │   ├── banner.png
│   │   └── logo.png
│   └── i18n
│       ├── en
│       │   └── localization.js
│       └── zh
│           └── localization.js
├── extends.js
├── extensions
│   ├── ccpool
│   │   └── CCNodePool.js
│   ├── dragonbones
│   │   ├── ArmatureCache.js
│   │   ├── ArmatureDisplay.js
│   │   ├── AttachUtil.js
│   │   ├── CCArmatureDisplay.js
│   │   ├── CCFactory.js
│   │   ├── CCSlot.js
│   │   ├── CCTextureData.js
│   │   ├── DragonBonesAsset.js
│   │   ├── DragonBonesAtlasAsset.js
│   │   ├── editor
│   │   │   ├── dragonbones-atlas-meta.js
│   │   │   └── dragonbones-meta.js
│   │   ├── index.js
│   │   ├── lib
│   │   │   ├── dragonBones.d.ts
│   │   │   └── dragonBones.js
│   │   └── webgl-assembler.js
│   └── spine
│       ├── AttachUtil.js
│       ├── Skeleton.js
│       ├── editor
│       │   ├── spine-asset.png
│       │   └── spine-meta.js
│       ├── index.js
│       ├── lib
│       │   ├── LICENSE
│       │   ├── spine.d.ts
│       │   └── spine.js
│       ├── skeleton-cache.js
│       ├── skeleton-data.js
│       ├── skeleton-texture.js
│       ├── spine-assembler.js
│       ├── track-entry-listeners.js
│       └── vertex-effect-delegate.js
├── external
│   ├── box2d
│   │   └── box2d.js
│   ├── cannon
│   │   └── cannon.js
│   └── socketio
│       ├── socket.io.js
│       └── socket.io.min.js
├── gulp
│   ├── browserify_prelude.js
│   ├── tasks
│   │   ├── buildDebugInfos.js
│   │   ├── engine.js
│   │   ├── test.js
│   │   └── watch.js
│   └── util
│       ├── create-bundler.js
│       ├── fix-jsb-javascriptcore.js
│       ├── handleErrors.js
│       └── utils.js
├── gulpfile.js
├── index.js
├── licenses
│   ├── LICENSE
│   ├── LICENSE_cocos2d-html5.txt
│   ├── LICENSE_cocos2d-x.txt
│   ├── LICENSE_spine.txt
│   ├── LICENSE_tslib.txt
│   └── LICENSE_zlib.js.txt
├── modules.json
├── package.json
├── polyfill
│   ├── array-buffer.js
│   ├── array.js
│   ├── bind.js
│   ├── misc.js
│   ├── number.js
│   ├── object.js
│   ├── polyfill.d.ts
│   ├── string.js
│   └── typescript.js
├── predefine.js
├── test
└── tsconfig.json
```