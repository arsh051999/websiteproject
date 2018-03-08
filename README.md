# adminchangepassword
<%@ Page Title="" Language="C#" MasterPageFile="~/admin.master" AutoEventWireup="true" CodeFile="adminchangepassword.aspx.cs" Inherits="adminchangepassword" %>

<asp:Content ID="Content1" ContentPlaceHolderID="head" Runat="Server">
</asp:Content>
<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" Runat="Server">
<table class="table"><tr><td>
    <asp:Label ID="Label1" runat="server" Text="Old password"></asp:Label></td>
    <td>
        <asp:RequiredFieldValidator ID="RequiredFieldValidator1" runat="server" 
            Display="Dynamic" ErrorMessage="*"></asp:RequiredFieldValidator>
        <asp:TextBox ID="tboldpassword" runat="server" CssClass="form-control"></asp:TextBox>
    </td></tr>
    <tr><td>
        <asp:Label ID="Label2" runat="server" Text="New password"></asp:Label>
    </td><td>
            <asp:RequiredFieldValidator ID="RequiredFieldValidator2" runat="server" 
                Display="Dynamic" ErrorMessage="*"></asp:RequiredFieldValidator>
        <asp:TextBox ID="tbnewpassword" runat="server" CssClass="form-control"></asp:TextBox>
    </td>
    </tr><tr>
    <td>
        <asp:Label ID="Label3" runat="server" Text="Confirm password" 
            CssClass="form-control"></asp:Label></td>
        <td>
            <asp:RequiredFieldValidator ID="RequiredFieldValidator3" runat="server" 
                Display="Dynamic" ErrorMessage="*"></asp:RequiredFieldValidator>
            <asp:CompareValidator ID="CompareValidator1" runat="server" 
                ControlToCompare="tbnewpassword" ControlToValidate="confirmpassword" 
                Display="Dynamic" ErrorMessage="password does not match"></asp:CompareValidator>
            <asp:TextBox ID="confirmpassword" runat="server" CssClass="form-control"></asp:TextBox> </td></tr>
            <tr><td>
                <asp:Button ID="Button1" runat="server" Text="Submit" CssClass="form-control" 
                    onclick="Button1_Click" /> </td>
                    <td>
                <asp:Label ID="Label4" runat="server" Text=""></asp:Label>
                </td></tr>
               
</table>
    <asp:SqlDataSource ID="SqlDataSource1" runat="server"></asp:SqlDataSource>
</asp:Content>
