# Internet-Connection-Message-Display


// Message Display
            if let window = UIApplication.shared.delegate?.window {
                if var viewController = window?.rootViewController {
                    // handle navigation controllers
                    if(viewController is UINavigationController){
                        viewController = (viewController as! UINavigationController).visibleViewController!
                        print(viewController.nibName as Any)
                        
                var bottomSafeAreaHeight: CGFloat = 0
                if #available(iOS 11.0, *) {
                    let window = UIApplication.shared.windows[0]
                    let safeFrame = window.safeAreaLayoutGuide.layoutFrame
                    bottomSafeAreaHeight = window.frame.maxY - safeFrame.maxY
                }
                        
                COMMONCLASS.sharedInstance.HideHUD()
                lblForInternetConntection.frame = CGRect(x: 0 , y: UIScreen.main.bounds.size.height - (50 + bottomSafeAreaHeight), width: UIScreen.main.bounds.size.width, height: 50)
                lblForInternetConntection.backgroundColor = .red
                lblForInternetConntection.text = "No Internet Connection"
                lblForInternetConntection.textAlignment = .center
                lblForInternetConntection.textColor = .white
                viewController.view.addSubview(lblForInternetConntection)
                    }
                }
            }
