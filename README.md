# AP18110010326-CD-LAB


<?xml version="1.0" encoding="UTF-8"?>
<!-- Created with Jaspersoft Studio version 6.20.0.final using JasperReports Library version 6.20.0-2bc7ab61c56f459e8176eb05c7705e145cd400ad  -->
<jasperReport xmlns="http://jasperreports.sourceforge.net/jasperreports" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://jasperreports.sourceforge.net/jasperreports http://jasperreports.sourceforge.net/xsd/jasperreport.xsd" name="Simple_Blue" pageWidth="595" pageHeight="842" columnWidth="535" leftMargin="20" rightMargin="20" topMargin="20" bottomMargin="20" uuid="87184d54-32bd-42fc-a192-1b72c1975136">
	<property name="com.jaspersoft.studio.data.sql.tables" value=""/>
	<property name="com.jaspersoft.studio.data.defaultdataadapter" value="Sample DB"/>
	<queryString language="SQL">
		<![CDATA[select * from address]]>
	</queryString>
	<field name="ID" class="java.lang.Integer">
		<property name="com.jaspersoft.studio.field.name" value="ID"/>
		<property name="com.jaspersoft.studio.field.label" value="ID"/>
		<property name="com.jaspersoft.studio.field.tree.path" value="ADDRESS"/>
	</field>
	<field name="FIRSTNAME" class="java.lang.String">
		<property name="com.jaspersoft.studio.field.name" value="FIRSTNAME"/>
		<property name="com.jaspersoft.studio.field.label" value="FIRSTNAME"/>
		<property name="com.jaspersoft.studio.field.tree.path" value="ADDRESS"/>
	</field>
	<field name="LASTNAME" class="java.lang.String">
		<property name="com.jaspersoft.studio.field.name" value="LASTNAME"/>
		<property name="com.jaspersoft.studio.field.label" value="LASTNAME"/>
		<property name="com.jaspersoft.studio.field.tree.path" value="ADDRESS"/>
	</field>
	<field name="STREET" class="java.lang.String">
		<property name="com.jaspersoft.studio.field.name" value="STREET"/>
		<property name="com.jaspersoft.studio.field.label" value="STREET"/>
		<property name="com.jaspersoft.studio.field.tree.path" value="ADDRESS"/>
	</field>
	<field name="CITY" class="java.lang.String">
		<property name="com.jaspersoft.studio.field.name" value="CITY"/>
		<property name="com.jaspersoft.studio.field.label" value="CITY"/>
		<property name="com.jaspersoft.studio.field.tree.path" value="ADDRESS"/>
	</field>
	<background>
		<band/>
	</background>
	<title>
		<band height="72">
			<frame>
				<reportElement mode="Opaque" x="-20" y="-20" width="595" height="92" backcolor="#006699" uuid="51996020-11f8-4fc0-8706-bc2c74b23354"/>
				<staticText>
					<reportElement x="20" y="20" width="234" height="43" forecolor="#FFFFFF" uuid="ff0785ce-03a0-4380-8682-957e063689ec"/>
					<textElement>
						<font size="34" isBold="true"/>
					</textElement>
					<text><![CDATA[TITLE]]></text>
				</staticText>
				<staticText>
					<reportElement x="395" y="43" width="180" height="20" forecolor="#FFFFFF" uuid="05a3ce21-e24e-41ac-87b9-bc85a00c493f"/>
					<textElement textAlignment="Right">
						<font size="14" isBold="false"/>
					</textElement>
					<text><![CDATA[Add a description here]]></text>
				</staticText>
			</frame>
		</band>
	</title>
	<pageHeader>
		<band height="13"/>
	</pageHeader>
	<columnHeader>
		<band height="21">
			<line>
				<reportElement x="-20" y="20" width="595" height="1" forecolor="#666666" uuid="fc75c4d6-65bb-4657-b6f0-e7fe28c99a45"/>
			</line>
			<staticText>
				<reportElement mode="Opaque" x="0" y="0" width="111" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="dcfc065e-0efd-4ad7-a56e-fc1be6813b17">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="550e4ca5-b19c-4568-943f-d59755fbea6c"/>
				</reportElement>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[ID]]></text>
			</staticText>
			<staticText>
				<reportElement mode="Opaque" x="111" y="0" width="111" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="d3f60929-daa2-4555-8bdf-83418582ed7d">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="a59a453e-9eac-4c25-ad8e-ca5c1fd24833"/>
				</reportElement>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[FIRSTNAME]]></text>
			</staticText>
			<staticText>
				<reportElement mode="Opaque" x="222" y="0" width="111" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="ee4b7744-6a16-4238-807a-b435cd5da622">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="5f591a92-c083-4aa8-888c-12b5ea5f6321"/>
				</reportElement>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[LASTNAME]]></text>
			</staticText>
			<staticText>
				<reportElement mode="Opaque" x="333" y="0" width="111" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="4ab1b382-1245-418b-a39d-a108a7a5d835">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="2fc21ace-09ae-46d6-a0a0-c3b0ae4cd80a"/>
				</reportElement>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[STREET]]></text>
			</staticText>
			<staticText>
				<reportElement mode="Opaque" x="444" y="0" width="111" height="20" forecolor="#006699" backcolor="#E6E6E6" uuid="9060d23a-9dca-41f4-9e8a-ffb8c28584ab">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="c28da2a7-0342-4f9b-98f6-8decdbac7226"/>
				</reportElement>
				<textElement textAlignment="Center">
					<font size="14" isBold="true"/>
				</textElement>
				<text><![CDATA[CITY]]></text>
			</staticText>
		</band>
	</columnHeader>
	<detail>
		<band height="20">
			<line>
				<reportElement positionType="FixRelativeToBottom" x="0" y="19" width="555" height="1" uuid="d3d039b4-25ee-4ad4-921f-8a1d060bb6b6"/>
			</line>
			<textField textAdjust="StretchHeight">
				<reportElement x="0" y="0" width="111" height="20" uuid="9877d7cf-539f-47f0-b12d-a8fa524acae4">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="550e4ca5-b19c-4568-943f-d59755fbea6c"/>
				</reportElement>
				<textElement>
					<font size="14"/>
				</textElement>
				<textFieldExpression><![CDATA[$F{ID}]]></textFieldExpression>
			</textField>
			<textField textAdjust="StretchHeight">
				<reportElement x="111" y="0" width="111" height="20" uuid="09ed689e-8490-4a79-8a83-aa8365495cec">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="a59a453e-9eac-4c25-ad8e-ca5c1fd24833"/>
				</reportElement>
				<textElement>
					<font size="14"/>
				</textElement>
				<textFieldExpression><![CDATA[$F{FIRSTNAME}]]></textFieldExpression>
			</textField>
			<textField textAdjust="StretchHeight">
				<reportElement x="222" y="0" width="111" height="20" uuid="8432c12a-48bd-4fd8-8013-12f9c0dda703">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="5f591a92-c083-4aa8-888c-12b5ea5f6321"/>
				</reportElement>
				<textElement>
					<font size="14"/>
				</textElement>
				<textFieldExpression><![CDATA[$F{LASTNAME}]]></textFieldExpression>
			</textField>
			<textField textAdjust="StretchHeight">
				<reportElement x="333" y="0" width="111" height="20" uuid="d2be00c6-cf31-4cee-b8ff-dd8f482eb08c">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="2fc21ace-09ae-46d6-a0a0-c3b0ae4cd80a"/>
				</reportElement>
				<textElement>
					<font size="14"/>
				</textElement>
				<textFieldExpression><![CDATA[$F{STREET}]]></textFieldExpression>
			</textField>
			<textField textAdjust="StretchHeight">
				<reportElement x="444" y="0" width="111" height="20" uuid="c19930a0-b868-47b7-b8dc-58499d6ae370">
					<property name="com.jaspersoft.studio.spreadsheet.connectionID" value="c28da2a7-0342-4f9b-98f6-8decdbac7226"/>
				</reportElement>
				<textElement>
					<font size="14"/>
				</textElement>
				<textFieldExpression><![CDATA[$F{CITY}]]></textFieldExpression>
			</textField>
		</band>
	</detail>
	<columnFooter>
		<band/>
	</columnFooter>
	<pageFooter>
		<band height="17">
			<textField>
				<reportElement mode="Opaque" x="0" y="4" width="515" height="13" backcolor="#E6E6E6" uuid="838fdbe8-bfcb-41ce-a792-cb701f2cb8c1"/>
				<textElement textAlignment="Right"/>
				<textFieldExpression><![CDATA["Page "+$V{PAGE_NUMBER}+" of"]]></textFieldExpression>
			</textField>
			<textField evaluationTime="Report">
				<reportElement mode="Opaque" x="515" y="4" width="40" height="13" backcolor="#E6E6E6" uuid="202f4911-0084-4bed-91d6-2727f0fe42ab"/>
				<textFieldExpression><![CDATA[" " + $V{PAGE_NUMBER}]]></textFieldExpression>
			</textField>
			<textField pattern="EEEEE dd MMMMM yyyy">
				<reportElement x="0" y="4" width="100" height="13" uuid="10914521-755a-4ebc-8a68-dccbeaa38eb0"/>
				<textFieldExpression><![CDATA[new java.util.Date()]]></textFieldExpression>
			</textField>
		</band>
	</pageFooter>
	<summary>
		<band/>
	</summary>
</jasperReport>
