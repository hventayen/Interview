import React, { useState } from "react";
/*still need to download files of Core UI*/
import LoginForm from "./LoginForm";
import Dashboard from "./Dashboard";

export default function App() {
  const [auth, setAuth] = useState({
    token: "",
    user: {},
    meta: {}
  })

  const onLoginSuccess = auth => {
    setAuth(auth);
  };

  const onLogOut = e => {
    setAuth({
      token: "",
      user: {},
      meta: {}
    });
  };

  const currentPage = () => {
    return auth.token ? (
      <Dashboard />
    ) : (
      <LoginForm onLoginSuccess={onLoginSuccess} />
    );
  }

  return (
    <div>
      <nav className="navbar navbar-expand navbar-dark bg-info">
        <a className="navbar-brand mr-auto" href="#">
          AppCo
        </a>

        {auth.token && (
          <ul className="navbar-nav">
            <li className="nav-item active">
              <a className="nav-link" href="#">
                Home <span className="sr-only">(current)</span>
              </a>
            </li>
            <li className="nav-item">
              <CCard>
                <CCardHeader>Alert</CCardHeader>
                <CCardText>
                Your email was involved in a breach on the following sites:
                </CCardText>
                this.props.breachedAccounts.map((date, name) => {
                  return(
                    
                  );
                })
                <CCardText>
                Although your information on our site is safe, we
recommend you change your password in case your AppCo
account shares a password with any of the sites above.
                </CCardText>
                <CButton href="#">Change Password</CButton>
                <CButton href="#">Dismiss</CButton>
              </CCard>
              <a className="nav-link" href="#">
                Tasks
              </a>
            </li>
            <li className="nav-item">
              <a className="nav-link" onClick={onLogOut}>
                Log out
              </a>
            </li>
          </ul>
        )}
      </nav>
      <div className="container">{currentPage()}</div>
    </div>
  );
}
