# BackToBack

// back btn
        if let controller = self.storyboard?.instantiateViewController(withIdentifier: "HomepageViewController") as? HomepageViewController {
            
            let viewcontrollers = self.navigationController?.viewControllers
            
            var isExist = false
            
            for viewcontroller in viewcontrollers! {
                
                if viewcontroller.isKind(of: HomepageViewController.self) {
                    
                    isExist = true
                    
                    break
                    
                }
                
            }
            
            if isExist == true {
                
                self.navigationController?.popViewController(animated: true)
                
            } else {
                
                self.navigationController?.viewControllers.insert(controller, at: (viewcontrollers?.count)!)
                
                self.navigationController?.popToViewController(controller, animated: true)
                
            }
        }
